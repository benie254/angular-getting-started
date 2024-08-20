# Getting Started with Angular

A guide for getting started with Angular by installing Angular CLI, creating an Angular project, and running the Angular server.

## Pre-requisites

In this guide, I’m assuming that you have the following installed on your machine:

- [Node.js version 18.9.1 or later](https://github.com/nvm-sh/nvm.git)
- [VSCode](https://code.visualstudio.com/docs/setup/linux)

## 1. Install Angular CLI

The Angular CLI enables you to run Angular commands from your terminal.

- Run the following command to install the Angular CLI globally:

  ```
  npm install -g @angular/cli
  ```

## 2. Create an Angular Project

An Angular project is a workspace we will use to build an Angular application. This workspace also provides a suitable environment for running Angular commands.

- Run the following command to create a new Angular project:

  ```
  ng new project-name-here
  ```

- Replace `project-name-here` with your preferred name for the project.

What happens after running the above command?

- Angular creates a folder with the name you used to initialize the project, e.g. `project-name-here`
- If you used your preferred project name instead of `project-name-here`, that’s the name of the folder that Angular will create.
- Inside the above folder, Angular will also auto-generate several files and directories. We will analyze these files and directories in the next subsection, **Angular Folder Structure**.
