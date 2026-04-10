When making a callout from a method, it waits for the external service to send back the callout response before. executing subsequent lines of code.

A callout must not block the trigger proces while waiting for the response.

You can place the callout code in an asyncronous method with the @future(callout=true) annotation. This way, the callout runs on a separate thread, and the execution of the calling method isn´t blocked.