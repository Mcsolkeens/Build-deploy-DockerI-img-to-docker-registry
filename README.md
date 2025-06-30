DOCKER IMAGE BUILD AND DEPLOYMENT USING GITHUB ACTIONS
PROJECT SUMMARY 
This Docker deployment pipeline for a React app automates the following steps:
-Takes the developer’s code pushed to the GitHub repository.
-Uses GitHub Actions to checkout the code on a runner.
-Dockerizes the React app using a Dockerfile (must be present in the repo).
-Builds a Docker image from the code.
-Tags the image appropriately for Docker Hub or another container registry.
-Authenticates with Docker Hub using secure credentials.
-Pushes the built container image to the specified Docker registry.

 PREREQUISITES (Local Setup)
- Install Git
- Set up GIT(for first time)
- Create Docker Hub Account
- 
🔐 Security Considerations Summary
✅ Store Docker credentials as GitHub Secrets (USERNAME, PASSWORD)

✅ Use specific action versions to avoid untrusted updates

✅ Add branch protection rules to master to prevent unauthorized code from triggering deployments







