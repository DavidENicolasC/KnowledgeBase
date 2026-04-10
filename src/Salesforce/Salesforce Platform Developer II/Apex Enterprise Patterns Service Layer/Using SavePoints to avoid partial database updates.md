
Use a syntax as follows:

```
SavePoint savePoint = Database.setSavePoint();
try {
	update Accounts;
	update RelatedContacts;
} catch(Exception exception) {
	Database.rollback(savePoint);
	throw exception
}
```