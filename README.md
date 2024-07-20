---
date-created: 20231130
tags:
- docker
- skopeo
- aidit
- disco
- disconnected
- transfer
- offline
- docker/registry
- registry
- nexus
- docker/img
- docker/image
---

# AIDIT: Air-gapped Image Docker Image Transfer
## Overview

AIDIT is a Bash script designed to assist with transferring Docker images to and from air-gapped (disconnected) environments. It utilizes the Skopeo tool to handle image transfers securely.

## Features

- **On-premises Image Handling:** AIDIT facilitates the movement of Docker images within on-premises environments.
- - **Air-gapped Support:** The script is specifically tailored for environments that are disconnected from the internet.
- - **Image Copying and Pushing:** AIDIT allows for both copying single images and pushing directories of images to a specified Docker repository.
## Prerequisites

- **Skopeo:** Ensure Skopeo is installed on your system. You can find Skopeo installation instructions [here](https://github.com/containers/skopeo#installation).
## Usage

```bash
./aidit.sh [-d <image_directory>] [-r <repository>] [-f <image_list_file>] <image_entry>
```

- `-d <image_directory>`: Specify the directory containing Docker images.
- - `-r <repository>`: Specify the Docker repository for pushing images.
- - `-f <image_list_file>`: Provide a file containing a list of Docker image entries.
### Examples

1. Copy a single image:
2.     ```bash
3.     ./aidit.sh myregistry/myimage:tag
4.     ```
5. Copy images from a directory to a repository:
6.     ```bash
7.     ./aidit.sh -d /path/to/images -r myregistry
8.     ```
9. Copy images listed in a file:
10.     ```bash
11.     ./aidit.sh -f image_list.txt
12.     ```
## License

This script is licensed under the [MIT License](LICENSE).

## TODO

- [ ] Migrate to DevOps Toolbox
