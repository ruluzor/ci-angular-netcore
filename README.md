### Pipeline for Angular and Dotnet apps on Github Actions

In order to adapt a pipeline to an Angular and Dotnet project in Github Actions we need to perform the following steps:

- #### In the project

  - Include the **.github** folder at the root of the project, in this way when the changes are uploaded the pipelines will be launched according to the desired configuration.

  - Include the javascript files **bump_version.js** and **current_version.js** which within the pipeline will extract the current version and the type of version to increase according to certain criteria.

-#### on Github

  - A Personal access token must be generated from the settings panel which will be used in the secrets of each repository.

  - Each repository must include a TOKEN_ACTION style secret, which will be used by the corresponding **.yml** files.

  - For the protection of branches, said protection must first be enabled in the configuration of each repository, once enabled, the ideal is that changes are not allowed to be uploaded to the main branch except by means of a change request (pull request). For this, the first option will be enabled.



### Pipeline para aplicaciones Angular y .Net sobre Github Actions

Para poder adaptar un pipeline a un proyecto Angular y .Net en Github Actions necesitamos realizar los siguientes pasos:

- #### En el proyecto

  - Incluir la carpeta **.github** a la raiz del proyecto, de esta manera cuando se suban los cambios se lanzarán los pipelines según la configuración deseada.

  - Incluir los archivos javascript **bump_version.js** y **current_version.js** los cuales dentro de la pipeline extraerán la versión actual y el tipo de versión a incrementar según unos criterios determinados.

- #### En Github

  - Se debe generar un Personal access token desde el panel de settings el cual será utilizado en los secrets de cada repositorio.

  - En cada repositorio se debe incluir un secret del estilo TOKEN_ACTION, el cual será utilizado por los archivos **.yml** correspondientes.

  - Para la protección de ramas primero se debe habilitar dicha protección en la configuración de cada repositorio, una vez habilitada, lo ideal es que no se dejen subir cambios a la rama principal salvo mediante peticion de cambios (pull request). Para ello se habilitará la primera opción.