Tauri generates JSON schemas with all the permissions available to your application through `tauri-build`, allowing autocompletion in your IDE.

To use a schema, set the `$schema` property in your configuration file (either .json or .toml) to one of the platform-specific schemas located in the `gen/schemas` directory. 

Usually you will set it to `../gen/schemas/desktop-schema.json` or `../gen/schemas/mobile-schema.json` though you can also define a capability for a specific target platform.