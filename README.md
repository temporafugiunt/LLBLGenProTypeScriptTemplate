# LLBLGenProTypeScriptTemplate
A simple template to generate TypeScript definitions for LLBLGen Pro Entity Definitions.

### Required NPM Installations

This template defines TypeScript class definitions which utilize two external libraries for serialization and deserialization into  strongly typed class definitions from dynamic JSON definitions returned by RESTFul APIs:

The work of these libraries is outlined in this useful article by the original author of json-typescript-mapper:
http://cloudmark.github.io/Json-Mapping/

	npm i reflect-metadata –save
	npm i @types/reflect-metadata –save
	npm i json-typescript-mapper --save

These files should be placed in the LLBLGen Pro installation directory in the directory structure defined in the repository. The LLBLGen Pro installation directory at the time of this writing is:

	C:\Program Files (x86)\Solutions Design\LLBLGen Pro v5.2
  
Once placed in that directory you will have a new `Selected preset` when excuting `Generate Source-code Generation (F7)` if you select the `Edit Selected Task Specifics` button.

You should select the new `CUSTOM.TypeScript.General` Preset for the `C#` language. This will then select the `CUSTOM.TemplateBindings.TypeScript.NET35` template binding as defined in the `Advanced...` tab.

This will then create in your output directory a `shared` subdirectory where the TypeScript model definitions (all with the names[EntityName].model.ts) will be defined.
