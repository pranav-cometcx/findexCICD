# Salesforce DX Project: Next Steps

This is Salesforce CRM Repo

Sample PR Body

[text](pull_request_template.md)


Procedure
1. All developers will checkout a feature branch from master and start building code on that branch

2. After finishing development, they will raise a PR from feature branch to the Merge branch. 
    a. This will run a git actions pipeline which will do a validate run into Merge Sandbox. 
    b. Once validated, the PR will be available to merge into the Merge branch which will run a pipeline to deploy ONLY the changes into the Merge Sandbox

3. For a SIT Release, we create a SIT release branch consisting of all feature branches ready to go into UAT. We then open a PR for the release branch to SIT
    a. This will run a git actions pipeline which will do a validate run into SIT Sandbox. 
    a. Once validated, the PR will be available to merge into the SIT branch which will run a pipeline to deploy all the changes into the SIT Sandbox

4. For a UAT Release, we create a UAT release branch consisting of all feature branches ready to go into UAT. We then open a PR for the release branch to UAT
    a. This will run a git actions pipeline which will do a validate run into UAT Sandbox. 
    a. Once validated, the PR will be available to merge into the UAT branch which will run a pipeline to deploy all the changes into the UAT Sandbox

5. For a Prod Release, we create a Prod release branch consisting of all feature branches ready to go into Prod. We then open a PR for the release branch to UAT
    a. This will run a git actions pipeline which will do a validate run into UAT Sandbox. 
    a. Once validated, the PR will be available to merge into the UAT branch which will run a pipeline to deploy all the changes into the Prodution Instance

6. For a hot-fix as well, same process as above is followed.
