Test using mixed DML calls are not allowed and fail.
You need to delete data manually if you write only to the big object.
To contain test DML calls to the targeting big object, use a mocking framework with the Apex stub API instead.

