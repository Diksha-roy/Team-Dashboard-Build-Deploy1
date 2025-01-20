# Team-Dashboard:Build-Deploy
### Overview
This document outlines the process for creating and managing a **Team Management Dashboard**. The project utilizes **Next.js**, **TypeScript**, and **Tailwind CSS**. The application is packaged using **Docker** and will be hosted on **Vercel**.

The dashboard is designed for managing tasks and teams, and works seamlessly across all devices. It is a fully functional and deployable application.


# Table of Contents

1. [Overview](#overview)
2. [Prerequisites](#prerequisites)
3. [Setting Up the Project](#setting-up-the-project)
   - [Step 1: Open the Vs code](#step-1-install-development-tools)
   - [Step 2: Create the next js app](#step-2-clone-the-repository)
   - [Step 3: Install Dependencies](#step-3-install-dependencies)
4. [Configuring the Project](#configuring-the-project)
   - [Step 4: Configure Tailwind CSS](#step-4-configure-tailwind-css)
   - [Step 5: Set Up Docker](#step-5-set-up-docker)
   - [Step 6: Configure GitHub](#step-6-configure-github)
5. [Running the Application Locally](#running-the-application-locally)
   - [Step 7: Run the Development Server](#step-7-run-the-development-server)
   - [Step 8: Build the Application](#step-8-build-the-application)
6. [Deploying the Application](#deploying-the-application)
   - [Step 9: Deploy to Vercel](#step-9-deploy-to-vercel)
7. [Usage Instructions](#usage-instructions)
   - [Home Page](#home-page)
   - [Task Management Page](#task-management-page)
8. [Additional Notes](#additional-notes)
9. [Useful Commands](#useful-commands)
10. [Links](#links)
    - [Live App](#live-app)
    - [Source Code](#source-code)
   
### Prerequisites:
### Prerequisites and Recommended Versions:

| Tool                   | Recommended Version             | Purpose                              |
|------------------------|---------------------------------|--------------------------------------|
| **Web Development Basics** | Any modern version            | For customizing the app             |
| **Node.js & npm**       | Node.js 18.x.x, npm 8.x.x       | To run the app                       |
| **TypeScript**          | TypeScript 4.x.x                | To ensure error-free code           |
| **Next.js**             | Next.js 12.x.x or latest        | For routing and rendering            |
| **Tailwind CSS**        | Tailwind CSS 3.x.x              | For responsive design                |
| **Docker**              | Docker 20.x.x or latest        | To run the app in any environment    |
| **Git & GitHub**        | Git 2.x.x or latest            | For version control                  |
| **Vercel**              | Latest Version                  | For hosting the app                  |
| **Visual Studio Code**  | Visual Studio Code 1.x.x or latest | For writing and editing the project code |


### Setting Up the Project

1. **Create a Project Directory**
   - Open your terminal and create a directory for the project:
     ```bash
     mkdir <your-project-name>
     cd <your-project-name>
     ```

2. **Open Visual Studio Code**
   - Open the directory in Visual Studio Code using the following command:
     ```bash
     code -r <your-project-name>
     ```

3. **Create a Next.js Application**
   - To create the Next.js app with TypeScript, Tailwind CSS, and other configurations, run:
     ```bash
     npx create-next-app@latest
     ```

4. **Installation Prompts**
   - During the installation process, you will be prompted to select the following options:
     ```
     What is your project named? my-app
     Would you like to use TypeScript? Yes / No
     Would you like to use ESLint? Yes / No
     Would you like to use Tailwind CSS? Yes / No
     Would you like your code inside a `src/` directory? Yes / No
     Would you like to use App Router? (recommended) Yes / No
     Would you like to use Turbopack for `next dev`? Yes / No
     Would you like to customize the import alias (`@/*` by default)? Yes / No
     What import alias would you like configured? @/*
     ```

   - Choose **Yes** for TypeScript, Tailwind CSS, App Router, and customizing import alias for a cleaner project structure.
  

  



    



