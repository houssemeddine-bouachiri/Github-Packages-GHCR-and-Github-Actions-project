
# Github Packages (GHCR) and Github Actions Project

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
