# veracode-jfrog-example
 example of Veracode integration in JFROG Pipelines

Author:https://github.com/bnreplah
Original:https://github.com/bnreplah/verademo
Duplicated and edited by me.

The folder with the main files is ".jfrog-pipelines" and should reside at the root of the repo. 

This example builds a Java Project then uploads using Veracode API Wrapper. 


essentially you would just need to set up:
 - A generic pipeline integration Object needs to be created where you would store the API ID and key, and possibly the SCA token as well if that is to be added to the pipeline.
 - Create a JFrog Artifactory Pipeline integration  Object as well like you have feel free to call it "myArtIntegration". If you want to upload the artifacts to the artifactory instead of just using the pipeline for the build and scan step.
 - The other thing that needs to be connected to the pipeline and created if it doesn't already exist is the github or scm integration object (Repo Sources) connection which will be used to connect to the build repo, it should be attached to a repo.