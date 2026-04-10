Use:
- `$Cache.Session`
- `$Cache.Org`
Same example applies for Org cache:
```[visualforce]
<apex:outputText value="{!$Cache.Session.ExPro.CurrencyCache.FavoriteCurrencyRate}"/>
```
You can´t omit `namespace.partition` prefix to reference default partition. Use local if a namespace is not defined for the org.
You can access to methods for data structures or variables for classes using the same syntax:
```[visualforce]
<apex:outputText value="{!$Cache.Session.local.MyPartition.numbersList.size}"/>
```
