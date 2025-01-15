# theTranslator.Web
Repo for dockerised translation Website using theTranslator.API

### Requirements

- Local install of Docker Desktop app. Up and running.
- A local copy of a Visual Studio suite, configured to process .Net 8 apps.

### Description

- .Net 8 MVC web app, just for simplicity.
- appsettings.json contains an entry for the API url:
	- "theTranslatorAPI": "https://localhost:44360/Translate"
	- This could be a secret key/value.
- Uses a simple jQuery ajax API call to retrieve the translation resuilt
	- Located in index.cshtml view.
	- Calls the dockerised API app.
- Web app has a fixed https port value assigned, to allow CORS operations between 2 domain separated apps: Web app and API service.
- Docker container configured for Windows OS, to make it simpler.

### Execution

- Clone the repository in your local machine.
- Open solution with Visual Studio.
- Make a rebuild to load any needed package.
- Just press F5 to run the Web app in a Docker Container.
- Web app will work independently of the API app, but no translation results 
- Needs the API app up and running in order to retrieve translations.
