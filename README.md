brjs-build-dependencies
=======================

This repo isn't intended to be cloned on any dev machine. It is used to provide public URLs for dependencies needed by the BRJS build which cannot be found on any public Maven repo. 

### Deploying an Artifact
1. To find the required arguments run `./gradlew`
2. Download the Artifact to the `brjs-build-dependencies` directory
3. Run `./gradlew -PdepGroup=org.my.group -PdepVersion=1.2.3 -PdepArtifact=someArtifact -PdepExtension=<artifact extension> -PdepFile=<path to file>`
  - for example to upload a new version of BRJS JSTestDriver run `./gradlew -PdepGroup=com.google -PdepVersion=1.3.3d-brjs7 -PdepArtifact=JsTestDriver -PdepExtension=jar -PdepFile=JSTestDriver.jar`
4. Delete the file downloaded in step 2
5. Commit and push the new artifacts inside `repo`
