To get a partition:
```[apex]
Cache.Org.getPartition('local.Example')
Cache.OrgPartition.get('key')
```

To set a cached value in a Partition:
```[apex]
Cache.OrgPartition.put('Key', 'value')
```
You can declare variables for one partition, like:
```[apex]
Cache.OrgPartition orgPartition = Cache.Org.getPartition('local.Example');
```
Use Cache.OrgPartition when managing cache values in just one partition.