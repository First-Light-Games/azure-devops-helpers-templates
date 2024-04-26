# FLG Azure Pipelines Templates
Some templates we use to help build our backend and game pipelines.

## Helpers

### download-artifact-with-build-number
Allows to download an artifact from another pipeline using only the build number.
Example of use: 
```yml
    - template: download-artifact-with-build-number.yml
      parameters:
        organizationName: "companyname" # If not provided will use current pipeline organization
        projectName: "projectName" # If not provided will use current pipeline project
        buildNumber: 2001
        pipelineName: "Game-Builds"
        artifactName: "GameDlls"
        downloadPath: $(System.ArtifactsDirectory)/Extracted
```