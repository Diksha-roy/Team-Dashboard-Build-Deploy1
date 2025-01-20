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
4. [setup the Project](#start-the-project)
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
  
   Step 1: Add Team Member Dummy Data
   Create a .js file for Dummy lib:

   Inside the data/ folder, create EmpDummyData.js:
  
   const empData = [
  {
    id: 1,
    name: "Amit",
    role: "Full Stack Developer",
    bio: "Passionate about building scalable web apps.",
    gender: "Male",
  },
  {
    id: 2,
    name: "Aarav",
    role: "Data Scientist",
    bio: "Loves extracting insights from big data.",
    gender: "Male",
  },
  {
    id: 3,
    name: "Ananya",
    role: "UI/UX Designer",
    bio: "Designs intuitive and user-friendly interfaces.",
    gender: "Female",
  },
  {
    id: 4,
    name: "Vihaan",
    role: "Cybersecurity Analyst",
    bio: "Keeps systems secure from vulnerabilities.",
    gender: "Male",
  },
  {
    id: 5,
    name: "Ishika",
    role: "Machine Learning Engineer",
    bio: "Works on AI models to solve real-world problems.",
    gender: "Female",
  },
  {
    id: 6,
    name: "Krishna",
    role: "DevOps Engineer",
    bio: "Automates workflows to streamline deployments.",
    gender: "Male",
  },
  {
    id: 7,
    name: "Neha",
    role: "Frontend Developer",
    bio: "Focuses on creating responsive web designs.",
    gender: "Female",
  },
  {
    id: 8,
    name: "Rohit",
    role: "Backend Developer",
    bio: "Specializes in server-side logic and APIs.",
    gender: "Male",
  },
  {
    id: 9,
    name: "Aisha",
    role: "Product Manager",
    bio: "Bridges the gap between tech and business needs.",
    gender: "Female",
  },
  {
    id: 10,
    name: "Aryan",
    role: "Mobile App Developer",
    bio: "Builds native apps for iOS and Android.",
    gender: "Male",
  },
  {
    id: 11,
    name: "Sanya",
    role: "Software Tester",
    bio: "Ensures quality by finding and fixing bugs.",
    gender: "Female",
  },
  {
    id: 12,
    name: "Kartik",
    role: "Cloud Engineer",
    bio: "Works on cloud solutions and infrastructure.",
    gender: "Male",
  },
  {
    id: 13,
    name: "Riya",
    role: "Database Administrator",
    bio: "Manages and optimizes databases.",
    gender: "Female",
  },
  {
    id: 14,
    name: "Aditya",
    role: "AI Specialist",
    bio: "Explores cutting-edge AI technologies.",
    gender: "Male",
  },
  {
    id: 15,
    name: "Meera",
    role: "Scrum Master",
    bio: "Facilitates Agile processes within teams.",
    gender: "Female",
  },
  {
    id: 16,
    name: "Arjun",
    role: "Blockchain Developer",
    bio: "Passionate about decentralized systems.",
    gender: "Male",
  },
  {
    id: 17,
    name: "Naina",
    role: "Technical Writer",
    bio: "Creates documentation for technical projects.",
    gender: "Female",
  },
  {
    id: 18,
    name: "Ravi",
    role: "Game Developer",
    bio: "Brings virtual worlds to life.",
    gender: "Male",
  },
  {
    id: 19,
    name: "Sara",
    role: "IoT Developer",
    bio: "Works on smart device integrations.",
    gender: "Female",
  },
  {
    id: 20,
    name: "Kabir",
    role: "IT Support Specialist",
    bio: "Solves IT issues to keep systems running.",
    gender: "Male",
  },
  {
    id: 21,
    name: "Tara",
    role: "AI Researcher",
    bio: "Explores new frontiers in artificial intelligence.",
    gender: "Female",
  },
  {
    id: 22,
    name: "Vikram",
    role: "Network Engineer",
    bio: "Ensures smooth and secure network operations.",
    gender: "Male",
  },
  {
    id: 23,
    name: "Simran",
    role: "Systems Analyst",
    bio: "Analyzes and improves system performance.",
    gender: "Female",
  },
  {
    id: 24,
    name: "Raj",
    role: "Embedded Systems Engineer",
    bio: "Works on hardware-software integration.",
    gender: "Male",
  },
  {
    id: 25,
    name: "Priya",
    role: "Tech Support Engineer",
    bio: "Provides technical assistance to clients.",
    gender: "Female",
  },
  {
    id: 26,
    name: "Harsh",
    role: "Web Developer",
    bio: "Crafts user-friendly websites and apps.",
    gender: "Male",
  },
  {
    id: 27,
    name: "Lina",
    role: "IT Project Manager",
    bio: "Oversees tech projects from start to finish.",
    gender: "Female",
  },
  {
    id: 28,
    name: "Amit",
    role: "Robotics Engineer",
    bio: "Develops intelligent robots for automation.",
    gender: "Male",
  },
  {
    id: 29,
    name: "Pooja",
    role: "QA Engineer",
    bio: "Tests applications to ensure flawless performance.",
    gender: "Female",
  },
  {
    id: 30,
    name: "Sahil",
    role: "AR/VR Developer",
    bio: "Builds immersive virtual experiences.",
    gender: "Male",
  },
];

export default empData;

step 2 Create a Dummy API:
In api/employees/route.ts , create an API to serve the team data:

import empData from "@/lib/EmpDummyData";
import { NextResponse } from "next/server";

export async function GET() {
  try {
    const response = NextResponse.json(empData);
    response.headers.set("Access-Control-Allow-Origin", "https://abs-uwxi.vercel.app"); 
    response.headers.set("Access-Control-Allow-Methods", "GET");

    return response;
  } catch (error) {
    console.error("Error fetching employees:", error);
    return NextResponse.json(
      { error: "Failed to fetch employees" },
      { status: 500 }
    );
  }
}    

Step 4: Build the Home Page
Fetch API Data in app/page.tsx:

"use client";
import Cards from "@/components/Cards";
import Navbar from "@/components/Navbar";
import { EmpDataProps } from "@/types/types";
import axios from "axios";
import { useEffect, useState } from "react";

export default function Dashboard() {
  const [data, setData] = useState<EmpDataProps[]>([]); 
  const [searchQuery, setSearchQuery] = useState<string>(""); 
  const [tasks, setTasks] = useState<any[]>([]); 

  const handleQueryChange = (query: string) => {
    setSearchQuery(query);
  };

  useEffect(() => {
    const fetchData = async () => {
      try {
        const res = await axios.get("https://abs-uwxi.vercel.app/api/employees");
        setData(res.data); // Assume data is an array of EmpDataProps
      } catch (error) {
        console.error("Error fetching data:", error);
      }
    };

    fetchData();
  }, []);

  useEffect(() => {
    const employeeTasks = data.map((item) => {
      const storedTasks = localStorage.getItem(`${item.name}-tasks`);
      return {
        employee: item,
        tasks: storedTasks ? JSON.parse(storedTasks) : [],
      };
    });
    setTasks(employeeTasks);
  }, [data]);



  const filteredData = data.filter((item) =>
    item.name.toLowerCase().includes(searchQuery.toLowerCase()) || 
     item.role.toLowerCase().includes(searchQuery.toLowerCase())
  );
  return (
    <>
      <Navbar handleQuery={handleQueryChange} />
      <div
        className="grid grid-cols-2 p-4 overflow-y-scroll"
        style={{ height: "calc(100vh - 100px)" }}
      >
        {filteredData.map((item: any) => (
          <div key={item.id}>
            {/* Pass only the tasks for the current employee */}
            <Cards
              imageUrl=""
              name={item.name}
              bio={item.bio}
              role={item.role}
              tasks={tasks.find(taskItem => taskItem.employee.id === item.id)?.tasks || []}
            />
          </div>
        ))}
      </div>
    </>
  );
}
Step 5: Build the Task Management Page

    Task Data in Local Storage:
        Use localStorage to save tasks.
        In app/tasks/index.tsx:
"use client";
import Cards from "@/components/Cards";
import Navbar from "@/components/Navbar";
import TaskCards from "@/components/TaskCards";
import { EmpDataProps } from "@/types/types";
import axios from "axios";
import { useEffect, useState } from "react";

export default function Page() {
  const [data, setData] = useState<EmpDataProps[]>([]); // Initialize as an array
  const [searchQuery, setSearchQuery] = useState<string>("");

  const handleQueryChange = (query: string) => {
    setSearchQuery(query);
  };

  useEffect(() => {
    const fetchData = async () => {
      try {
        const res = await axios.get("https://abs-uwxi.vercel.app/api/employees");
        setData(res.data);
      } catch (error) {
        console.error("Error fetching data:", error);
      }
    };

    fetchData();
  }, []);

  const filteredData = data.filter((item) =>
    item.name.toLowerCase().includes(searchQuery.toLowerCase()) || 
     item.role.toLowerCase().includes(searchQuery.toLowerCase())
  );

  return (
    <div>
      <Navbar handleQuery={handleQueryChange} />
      <div
        className="grid grid-cols-2 p-4  overflow-y-scroll"
        style={{ height: "calc(100vh - 100px)" }}
      >
        {filteredData.map((item: any) => (
          <div key={item.id}>
            <TaskCards
              // key={item.id}
              imageUrl=""
              name={item.name}
              bio={item.bio}
              role={item.role}
            />
          </div>
        ))}
      </div>
    </div>
  );
}

Step 6: Run the Application

    Start the development server:

    ```bash npm run dev```
    Open the app in your browser at http://localhost:3000.

    

