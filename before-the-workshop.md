# Before the Workshop

Before the workshop, please use this checklist to make sure your computer is set up to build and run NextGen in a Box (NGIAB). These instructions are specific for each operating system. If you have any questions, please don't hesitate to contact the workshop team. These instructions are compiled from the [NGIAB 101 training module](https://ngiab.ciroh.org/training-NGIAB-101/installation.html).

## System Requirements

- Administrative privileges
- Minimum 8 GB of RAM
- Windows, macOS, or Linux

## Windows

1. Make sure Windows Subsystem for Linux (WSL) is installed. If it is not, you can install it with this command:

   ```powershell
   wsl --install
   ```

2. Make sure Docker Desktop is installed. If it is not, you can install it from [Docker's official website](https://docs.docker.com/desktop/setup/install/windows-install/).
3. Verify your WSL and Docker installations.
   1. Launch Docker Desktop.
   2. Open your WSL terminal as administrator.
   3. Verify that Docker works as expected by running this command:

    ```bash
    docker run hello-world
    ```

    This should generate a message like this:

    ```text
    Hello from Docker!
    This message shows that your installation appears to be working correctly.
    ```

4. Within WSL, clone the NGIAB source code in your desired directory.

    ```bash
    cd /path/to/directory # navigate to your desired directory
    git clone https://github.com/CIROH-UA/NGIAB-CloudInfra.git
    ```

## macOS

1. Make sure Docker Desktop is installed. If it is not, you can install it from [Docker's official website](https://docs.docker.com/desktop/setup/install/mac-install/).
2. Verify your Docker installation.
   1. Launch Docker Desktop.
   2. Verify that Docker works as expected by running this command:

    ```zsh
    docker run hello-world
    ```

    This should generate a message like this:

    ```text
    Hello from Docker!
    This message shows that your installation appears to be working correctly.
    ```

3. Clone the NGIAB source code in your desired directory.

    ```zsh
    cd /path/to/directory # navigate to your desired directory
    git clone https://github.com/CIROH-UA/NGIAB-CloudInfra.git
    ```

## Linux

1. Make sure Docker Desktop is installed. If it is not, you can install it from [Docker's official website](https://docs.docker.com/desktop/setup/install/linux/).
2. Verify your Docker installation.
   1. Start the Docker service and verify that Docker works as expected with these commands:

    ```bash
    sudo systemctl start docker
    docker run hello-world
    ```

    This should generate a message like this:

    ```text
    Hello from Docker!
    This message shows that your installation appears to be working correctly.
    ```

3. Clone the NGIAB source code in your desired directory.

    ```bash
    cd /path/to/directory # navigate to your desired directory
    git clone https://github.com/CIROH-UA/NGIAB-CloudInfra.git
    ```

## Troubleshooting

### Docker not working in WSL

If you installed Docker before WSL, you will likely need to install a new WSL distribution and set it as your default.

 ```powershell
 wsl --install -d Ubuntu
 ```

### Git not installed

Please follow the installation instructions on the [official GitHub page](https://github.com/git-guides/install-git).
