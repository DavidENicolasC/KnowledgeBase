This can provide standard hooks to implement common domain logic for validation of records via a onValidate() method and defaulting field values via a onApplyDefaults() method.

You can also provide methods for create a new instance of the trigger handler logic for a domain class and passes in the sObject list, as Trigger.new.