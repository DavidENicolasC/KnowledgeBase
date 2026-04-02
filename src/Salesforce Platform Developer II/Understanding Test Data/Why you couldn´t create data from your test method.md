* Some standard objects aren´t creatable.
* Inserting duplicate records for sObjects that have fields with unique constraints results in an error. This can occur whether you are [[Using the IsTest(SeeAllData=True) annotation]] or not.
* Records that are created only after related records are commited to database.
* Chatter FeedTrackedChange and Field tracking history records can´t be created in test case require other sObject records to be commited first.