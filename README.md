# elixir-dockerfile

A drop-and-build Dockerfile for elixir projects.

# Usage

If you're running a standard mix-generate project all you should do is put a Dockerfile at the root of the project with the following directive:

```Dockerfile
FROM nanit/elixir:latest-onbuild
```

and you have a Docker image with your Elixir application ready to run.
