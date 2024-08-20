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

### A. Angular Folder Structure

Below is a standard Angular folder structure, auto-generated when you run `ng new project-name-here`:

```
.
├── public
├── src
│   ├── app
│   ├── index.html
│   ├── main.server.ts
│   ├── main.ts
│   ├── styles.scss
│   └── ...
├── angular.json
├── server.ts
├── tsconfig.app.json
├── tsconfig.spec.json
└── ...

```

Here is a breakdown of the purposes of the above directories and files:

- `public`

  - Used for storing assets, e.g. **images**, **fonts**, and **stylesheets**, among other non-code project resources.
  - You can access these assets directly from your components or stylesheets using relative paths, e.g. `assets/logo.png`

- `src`

  - The root directory of your project’s source code.

- `src/app`

  - Contains the core structure of your project.
  - This is where you will create your `components`, `routes`, `services`, and `utilities`, among other project resources.
  - This folder also contains the root `component` of your application, which encapsulates all other components.

- `src/index.html`

  - Serves as an entry point for your application.
  - Contains a basic HTML structure and encapsulates the `app component` or `root component`.
  - Since Angular apps are Single-Page Applications, the entire app runs within a single HTML page.
  - When users navigate through your app, the Angular `router` handles URL changes without reloading the entire app; it dynamically updates the content of the `index.html` file.

- `src/main.server.ts`

  - Enables server-side rendering **(SSR)**.
  - Serves as the entry point for rendering your Angular application on the server.
  - We will look further into **SSR** later on.

- `src/main.ts`

  - The main entry point of your application logic.
  - Serves your application on the browser side.

- `src/styles.scss`

  - Your root stylesheet.
  - You can write application-level and reusable styles in this file.
  - This file’s extension can also be `.css` or `.less`, depending on the stylesheet format you select(ed) while creating your Angular project.

- `angular.json`

  - Contains project configuration options such as development or production configs, test settings, deployment paths, and more.
  - It provides a blueprint for the Angular CLI to build, serve, and test your application.

- `server.ts`

  - Acts as the entry point for your server-side rendering (SSR) logic.
  - It sets up an Express server and configures it to handle rendering Angular components on the server.

- `tsconfig.app.json`

  - A configuration file that defines Angular compiler options for TypeScript code within the `src` directory, specifically targeting application code.

- `tsconfig.json`

  - The base TypeScript configuration file that applies to all TypeScript code in the project.

- `tsconfig.spec.json`

  - A configuration file for TypeScript in the context of unit tests.
