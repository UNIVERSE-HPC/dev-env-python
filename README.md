# VSCode devcontainer template: Python

Template project to allow students to edit, run and debug Python code in VSCode
using a consistent containerised environment.

## Launching in local VSCode

_Prerequesites: Install VSCode and Docker._

When you open this project folder in VSCode, accept the popup to open in a Dev
Container. Alternatively, you can run the editor command 'Dev Containers: Reopen
in Dev Container' at any time. Editor commands can be launched by pressing
Ctrl+Shift+P (or Cmd+Shift+P on Macos).

## Launching in GitHub Codespace

From your GitHub page, click on the hamburger icon (3 horizontal slashes) in the
top left of the page and select 'Codespaces'. Click on 'New Codespace' and
choose the repository you want to open. Use the defaults for the remaining
settings and click 'Create Codespace'. A web-based VSCode client will start and
build the dev container which will take some time on the initial run.

## Launching outside of a devcontainer

The launch scripts will run provided the correct dependencies are installed. See
`Dockerfile` for reference.

## Running and Debugging

This project is configured with a `launch.json` script that specifies the
Python code to run or debug. Click on the Run and Debug icon on VSCode sidebar
and click the Play icon in the debug panel.

## Maintenance

- `.devcontainer/devcontainer.json` specifies the Dockerfile, VSCode extensions
   and any other project settings. If you need to add another extension, the
   identifier can be found in the More Info section of its docs.
- `.devcontainer/Dockerfile` is the Dockerfile loaded to set up this
  environment. For this project it is a debian Python image. If changing this,
  ensure to use specific image versions otherwise it will pull 'latest' which
  may cause inconsistencies.
- `.vscode/launch.json` specifies the scenarios for running or debugging code.
  Each of the JSON dicts appears in the play icon in the Run and Debug panel.
  This is not limited to Python; the `"type"` field can be changed for different
  tools.
