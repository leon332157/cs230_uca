# Docker Environment

### Instructions for Setting Up Your Development Environment with a DevContainer

## Prerequisites
### Ensure you have [Docker](https://www.docker.com/get-started) installed for your platform:
- [Mac](https://hub.docker.com/editions/community/docker-ce-desktop-mac)
- [Windows](https://hub.docker.com/editions/community/docker-ce-desktop-windows)
- Linux? really? fine [here you go](https://docs.docker.com/install/linux/docker-ce/ubuntu/)

#### Install the [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension in VSCode. This extension allows you to use a Docker container as a full-featured development environment.

## Download:

[devcontainer.zip](devcontainer.zip)

## Follow these steps:

1. **Download and Extract the devcontainer zip file**
   - After downloading, keep it in a folder you frequently use, such as a course folder named `cs230`
2. **Copy the .devcontainer Folder**
   - If you can not see the folder, it is hidden because of the dot at the start, in this case, on Mac, press `Command+Shift+.`. On Windows, Select View > Show > Hidden items.
   - Copy this folder to the ROOT directory of your downloaded project starter code. 
3. **Open Your Project in VSCode**
    - Open Visual Studio Code.
    - Go to `File` > `Open Folder...` and select your project directory (the one where you just copied the `.devcontainer` folder).
4. **Reopen in Container**
   - Once your project folder is open in VSCode, you'll see a pop-up in the lower right corner asking if you want to reopen the folder to develop in a container. Click on `Reopen in Container`. If you don't see the pop-up, press `F1` to open the command palette, type `Remote-Containers: Reopen in Container`, and press enter.
  
   - VSCode will start building the Docker container based on the configuration specified in the `.devcontainer` folder. This process may take a few minutes, especially the first time, as it needs to download the Docker image and set up the environment.

5. **Wait for the Container to Build**
    - After initiating the build process, a terminal window in VSCode will show the progress of building the Docker container. Once the build is complete, VSCode will automatically connect to the container. This may take up to 15 minutes.

6. **Start Developing**
    - Once connected, you're now inside a fully configured development environment based on Docker. You can start installing dependencies, running your project, and coding as if you were on your local machine, but with the benefits of a consistent, containerized development environment.

### Troubleshooting

- Make a Piazza Post!
  
- If you encounter any issues during the container build process or while using the container, check the terminal output for errors. Common issues include problems with Docker not running or permissions issues related to accessing certain files.
- Ensure Docker is running before trying to reopen your project in a container.
- If VSCode does not automatically prompt you to reopen your project in a container, ensure the `.devcontainer` folder is at the root of your project and that the Remote - Containers extension is properly installed and enabled, you can also manually reopen current folder in devcontainer.