# Complete-CICD-Deployment

**Overview:**

In this project, 
If developer make any changes in github repo, it will trigger CI job of the jenkins which will pull the code from application repo and it will build and test the artifacts using maven, then static code analysis of artifact using sonarqube, then build and push docker image to dockerhub. After that scan docker image using trivy scan. Once above CI job will completed, our CD job will automatically triggered. It will update build number in the deployment yaml file on the gitops repo in github. Then argocd will pull the upodated manifest files from the gitops repo and it will deploy resources on aws EKS cluster.

In this repo I attached clear SOP Documentation to implement this project.
