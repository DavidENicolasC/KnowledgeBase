- Identifies business-critical operations before moving users to Salesforce
- Identifies minimal data set and configuration required to implement the operations
- Defines a data and configuration strategy based on the requirements
- Load the data as quickly as possible to reduce scope of synchronization

Consider the following:

- **Organization-wide sharing defaults** - When is private sharing model, system calculates sharing as record are being added. When is Public Read/Write sharing model, you can defer this processing until after cutover.
- **Complex object relationships** - The more lookups, the more checks the system has to perform. If you can establish some of these relationships in a later phase, loading go faster.
- **Sharing rules** - If you have ownership-based sharing rules to before loading data, each record requires sharing calculations when the owner belongs to a role or group defining data to be shared. Criteria-based sharing rules configured also requires sharing calculations.
- **Workflow rules, validation rules, triggers** - Can slow down processing if enabled during massive data loads.