# Dockerfile Bug: Using the `latest` tag

This repository demonstrates a common, yet often overlooked, error in Dockerfiles: using the `latest` tag for base images.  This can lead to unexpected behavior and inconsistencies in your builds.

The `Dockerfile_bug` shows the problematic code. The `Dockerfile_solution` provides a corrected version.

**Problem:** Using `latest` means your image will be built using whatever the latest version of Ubuntu happens to be.  Future updates to the base image could introduce breaking changes that break your application.

**Solution:** Pin your base image to a specific version using a tag like `20.04` or `22.04`. This ensures that your image will be consistent across builds.