# ApimCAppApi

Clone the project
git clone https://<username>@bitbucket.org/cellcardvasdev/apim_capp_api.git 

Build carbon application with registry sequences
./gradlew buildWSO2

Deploy the API
./gradlew deployAPI

Prior to deploying APIs in local environment, following environment variables should be set.

export ENVIRONMENT=local
export APIM_USER_LOCAL=admin;
export APIM_PWD_LOCAL=admin;
export APIM_PUBLISHER_EP_LOCAL=https://localhost:9443;
export APIM_TOKEN_EP_LOCAL=https://localhost:8243;
