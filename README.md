
# Github Packages (GHCR) and Github Actions Project

![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white&style=flat)
![GitHub](https://img.shields.io/badge/GitHub-181717?logo=github&logoColor=white&style=flat)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?logo=githubactions&logoColor=white&style=flat)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=flat)
![License](https://img.shields.io/badge/License-MIT-yellow)

This project demonstrates how to build, test, and deploy a Docker container to **GitHub Container Registry (GHCR)** using **GitHub Actions**.

<https://docs.github.com/en/actions>

<https://docs.github.com/en/packages/working-with-a-github-packages-registry/working-with-the-container-registry>

---

## Push an image to Github Packages (GHCR)

1. Create image

    ```
    docker build -t hello .
    ```

2. Create PAT on Github

3. Authenticate GHCR

    ```
    export CR_PAT=<TOKEN>
    echo $CR_PAT | docker login ghcr.io -u USERNAME --password-stdin
    ```

4. Tag and push our image to GHCR

    ```
    docker tag hello ghcr.io/username/hello:latest
    docker push ghcr.io/username/hello
    ```

## Use Github Actions to Publish a Docker image to Github Packages (GHCR)

1. Create repo - and Checkin our Dockerfile
2. Build your Github action workflow
3. Trigger our workflow

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

**Star this repo if it helped you!**
