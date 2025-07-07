

# 🚀 Build and Publish to Docker Registry

This GitHub Actions workflow automates the process of building a **Docker image from a React-based codebase** and pushing it to a Docker Hub repository. 

The workflow is triggered on every push to the `master` branch, enabling seamless and consistent container builds and deployments.

---

## 📌 What This Workflow Does

When changes are pushed to the `master` branch, this pipeline:

1. **Checks out the latest source code** for the React application.
2. **Authenticates with Docker Hub** using GitHub Secrets.
3. **Builds a Docker image** using the provided `Dockerfile`.
4. **Tags and pushes the image** to your Docker Hub repository.

This setup ensures the frontend application is always packaged and ready to deploy in a consistent Dockerized environment.


##  Required GitHub Secrets

| Secret Name | Description                  |
| ----------- | ---------------------------- |
| `USERNAME`  | Docker Hub username          |
| `PASSWORD`  | Docker Hub password or token |

Add these in your repo under **Settings > Secrets and variables**.

##  Docker Image Info

* **Build Context**: Assumes `Dockerfile` and React app source are in the root of the repo.
* **Image Tag (local)**: `app:v1`
* **Remote Image**: `mcsolkeens/app_dev`

##  Example Project Structure

```bash
.
├── Dockerfile              # Defines how the React app is built into an image
├── package.json            # React dependencies and scripts
├── public/
├── src/                    # React source code
└── .github/
    └── workflows/
        └── docker-publish.yml

## Before You Begin

* Ensure your `Dockerfile` correctly builds and serves the React app (e.g., using Node or Nginx).
* Make sure the Docker Hub repository exists (`$reponame/app_dev`) or can be created automatically.
* Configure required secrets in GitHub.









