Use `Cache.Session` and `Cache.SessionPartition` classes to access values in session cache.
`Cache.Session` - Manage any partition
Cache.SessionPartition - Manage only one partition

```[apex]
Cache.SessionPartition sessionPart = Cache.Session.getPartition('local.CurrencyCache');
sessionPart.put('FavoriteCurrency', 'JPY');
String cachedRate = (String) sessionPart.get('FavoriteCurrency');
```