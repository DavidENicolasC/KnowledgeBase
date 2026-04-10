The index defines the composite primary key for a big object. The fields defined in the index determine the big object's identity and ability to be queried.

At least a custom field is required in the index, and can have up to five custom fields total. Only required custom fields are allowed in an index.

Long Text Area fields can´t be included in the index.

Total number of characters across all text fields in an index can´t exceed 100.

Index can´t be modified or deleted.

SOQL can query only on the index's fields, in the order tou defined them in.

Details

| Field Name   | Description                                                                                                                                              |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Label**    | Used for refer to the index in the UI Name                                                                                                               |
| **API Name** | API Name for the Index                                                                                                                                   |
| **Index fields** | Set the index position and Index direction for each custom field included in the index. Position 1 for most frequently used filter parameter. Index Direction can be ascending or descending 