You can define any of the [[Understanding cache partitions]] as the default partition, but can only have one default partition. This enables to you to use shorthand syntax on that partition.

```
Cache.Org.put('namespace.partition.key', 0) -> Cache.Org.put('key', 0)
```

You can also use the `Cache.OrgPartition` class.