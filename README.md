# dsci522-dockerfile-practice

A practice repository for DSCI 522 demonstrating how to build a reproducible Python (`uv`) Docker image with pinned dependencies (`cowsay` and `numpy`) and automatically publish it to Docker Hub using GitHub Actions.

## Usage

Pull and run the image from Docker Hub:

```bash
docker run --rm jaylonhubc/dsci522-dockerfile-practice:latest uv run python -c "import cowsay, numpy; print(numpy.__version__)"
```

## Platform Support Note

This image is currently built for the linux/amd64 (x86_64) architecture only. If you are running on an ARM64 machine (such as Apple Silicon Macs or Raspberry Pi), specify the --platform linux/amd64 flag when running the container:

```bash
docker run --rm --platform linux/amd64 jaylonhubc/dsci522-dockerfile-practice:latest uv run python -c "import cowsay, numpy; print(numpy.__version__)"
```
