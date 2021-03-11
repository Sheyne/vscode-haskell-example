# Try Out Development Containers: Haskell

This is a sample project that lets you try out the **[VS Code Remote - Containers](https://aka.ms/vscode-remote/containers)** extension in a few easy steps.

> **Note:** If you're following the quick start, you can jump to the [Things to try](#things-to-try) section. 

## Setting up the development container

Follow these steps to open this sample in a container:

1. If this is your first time using a development container, please follow the [getting started steps](https://aka.ms/vscode-remote/containers/getting-started).

2. **Linux users:** Update `USER_UID` and `USER_GID` in `.devcontainer/Dockerfile` and `"runArgs": [ "-u", "1000" ]` in `.devcontainer/devcontainer.json` with your user UID/GID if not 1000 to avoid creating files as root.
    If you get a permission denied on Fedora or another SELinux enabled Linux Distribution you can, as a workaround, run `chcon -Rt svirt_sandbox_file_t $PWD` inside the `${workspaceFolder}` to fix the error. ([related Issue](https://github.com/microsoft/vscode-remote-release/issues/1333)

3. If you're not yet in a development container:
   - Clone this repository.
   - Press <kbd>F1</kbd> and select the **Remote-Containers: Open Folder in Container...** command.
   - Select the cloned copy of this folder, wait for the container to start, and try things out!

## Things to try

Once you have this sample opened in a container, you'll be able to work with it like you would locally.

> **Note:** This container runs as a non-root user with sudo access by default. Comment out `"runArgs":["-u", "1000"]` in `.devcontainer/devcontainer.json` if you'd prefer to run as root.

Some things to try:

1. **Edit:**
   - Open `src/Main.hs`
   - Try adding some code and check out the language features. Notice that you can hover over variables to see their type and Haddock information.
2. **Terminal:** Press <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>\`</kbd> and type `uname` and other Linux commands from the terminal window.
3. **Build, Run, and Debug:**
   - <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>p</kbd> and type run to run the current application with stack
   - <kbd>Ctrl</kbd>+<kbd>Shift</kbd>+<kbd>b</kbd> will build with stack
   
