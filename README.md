## Azure Durable Function starter framework
This starter framework is aimed for the video processing workloads using Python. Punch-in your code and hit `F5` to try it live

## Getting started
- Install [Azure Function Core Tools](https://go.microsoft.com/fwlink/?linkid=2135274) or `brew install azure-functions-core-tools@3` (for Mac OSX)
- Install [Azurite](https://github.com/Azure/Azurite) (local storage emulator): `npm install -g azurite@alpha`
- Switch connection strings in `local.settings.json` (it's a local storage emulator by default)
- Create a virtual environment for Python: `.venv\Scripts\activate` or `source .venv/bin/activate` for Mac OSX
- Restore dependencies from "requirements.txt": `pip install -r requirements.txt`
-Run a function: `func start`
>**NOTE:** Azurite tables are in development. The table alpha may work (the one suggested for installation above). To get a guaranteed result, connect to a live Azure Storage account for testing.


## Build for Docker
- Build a Docker image: `docker build -t test-func -f Dockerfile .` where "test-func" can be any name for your container
- Run Docker image: `docker run -p 8080:80 -it test-func`

>**NOTE:** Only Python 3.7 is supported by Azure Durable Functions