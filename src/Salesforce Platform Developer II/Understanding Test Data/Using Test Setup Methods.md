Are annotated with @testSetup. Are first executed before any test method. Data created and modified for test methods, including static data, are rolled back before each test method execution, as runs in separate threads.

Are supported only with the default data isolation mode for a Test Class. Are only available for the 24.0 and API versions only by the [[Data visibility for test code changes depending on API version]].

You can have only one test setup method per test class.

Errors in test setup method make the entire test class fail.

Code coverage is not calculated for calls not non-test methods from test setup methods.