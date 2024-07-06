[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/GvXCZgfk)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15343822&assignment_repo_type=AssignmentRepo)
# SE-Assignment-4
Assignment: GitHub and Visual Studio
Instructions:
Answer the following questions based on your understanding of GitHub and Visual Studio. Provide detailed explanations and examples where appropriate.

Questions:
Introduction to GitHub:

What is GitHub, and what are its primary functions and features? Explain how it supports collaborative software development.

GitHub is a web-based platform designed for version control and collaboration on software projects using Git. It allows developers to track changes in code,share codes with others,collaborate with multiple people on projects,create repositories which store and manage codebases,forking,creating your own personal copy of a repository, and contribute to open source projects, and manage software development projects.Additionally,GitHub has tools such as issues,pull requests and code review which support collaborative development.GitHub uses Git which makes sure changes are merged smoothly when many contributors work on the same project simultaneously.Developers can create branches for independent code development once ready,they merge changes back into the main branch preventing conflicts.GitHub also has collaboration tools like project boards and discussions allowing teams to connect successfully,plan work and document processes.

Repositories on GitHub:

What is a GitHub repository? Describe how to create a new repository and the essential elements that should be included in it.

A GitHub repository is a virtual storage space where you can store code,project's files,folders and history and track changes in a project.It is the centerpoint for documentation and collaborative work and contains code files,documentation,images,videos and configuration files.
how to create a new repository:
1.Create an account or Sign in to GitHub 
2.To create a new repository on the top right corner click on the "+" icon and select "new repository" 
3.Enter a name for your repository 
4.Add a brief description of the project which is optional 
5.Make the repository either public or private 
6.Initialize your project with a README file, check the box onscreen 
7.Choose an open-source license for your repository which defines what others can and cannot do with your code 
8.To exclude specific files or directories from the version control add a " .gitignore " file 
9.Create a directory for the code and add necessary files
10.Write a commit message describing your initial commit and click on "commit changes" and save
11.Click on the gear icon,go to repository's settings and set the default branch(master/main)

Version Control with Git:

Explain the concept of version control in the context of Git. How does GitHub enhance version control for developers?

Version control in the context of Git is the process of tracking and managing changes to files over time.Git tracks the changes to files over time,Working directory is where the changes are made,staging area prepares changes before committing and the local repository stores the history of the project.Branches are parallel versions of a project which let you work on different features independently without disturbing the main project until it is ready to merge.
GitHub enchances version control by:
Providing a powerful issue tracking system which enables developers to create,manage and issues related to their projects,this helps track bugs,feature requests and improvements effectively.Also, easy branching and merging for simultaneous feature development,integration with tools,centralised repository for storing and managing code and a large open-source community for sharing and learning this helps contribute and maintain code quality.GitHub's pull request system includes of comments,approvals and status checks which facilitates detailed code reviews ensuring high-quality contributions.


Branching and Merging in GitHub:
What are branches in GitHub, and why are they important? Describe the process of creating a branch, making changes, and merging it back into the main branch.

Branching in Git is a powerful way to manage and organize development in a collaborative environment.It allows multiple developers to work on different features,fixes or experiments simultaneously without conflicts.Branches isolate experimental changes,reducing risk of breaking the main codebase and allowing developers to test and validate changes before merging them back into the main branch.They are important as they enable teams to work efficiently and safely ensuring a stable and reliable codebase.
PROCESS:
1.Open the command prompt and navigate to the local repository using ' cd '
2.Create a new branch by running the command ' git branch <insert branch-name> ' 
3.To make sure the local repository is up-to-date with the remote repository use the command ' git pull origin main/master ' 
4.Run the command ' git checkout <insert branch-name> ' to switch from the current branch to a new branch
5.To make changes such as edit,delete or add new files run, ' git add <file-name> ' or ' git add . ' to add all files ,to stage changes
6.To commit changes run ' git commit -m "describe the changes made" '
7.Run ' git checkout main/master ' to switch back to the main branch
8.The command ' git merge <insert branch-name> ' merges the changes from the new branch back into the main branch
9.To push the updated main branch to the remote repository run ' git push origin main/master ' 

Pull Requests and Code Reviews:
What is a pull request in GitHub, and how does it facilitate code reviews and collaboration? Outline the steps to create and review a pull request.

A pull request is a request to merge changes from one branch into another.Pull requests let you tell others about changes that have been pushed to a branch in a repository on GitHub.It allows team members to examine code changes,comment on specific lines and provide feedback and suggesting improvements before merging into main branch.Pull requests provide a dedicated platform for discussing changes which helps keep conversations organized,it serves as a record of why and how were changes made for future reference and also knowledge sharing.CI/CD are integrated for running tests and checks automatically,ensuring code quality and functionality before merging.
CREATING A PULL REQUEST:
1.Fork the repository by clicking the 'fork' button on GitHub and copy the code by clicking the 'code' button and copy the url
2.Clone the forked repository into your local machine using ' git clone <insert url of repository> '
3.Create a new branch,modify files,commit changes and push commited changes to the remote repository 
4.Navigate to the repository on GitHub and click on the "new pull request" button
5.Choose the branch with your changes as the 'head' branch and main branch(main/master) as the base branch
6.Provide a title and description of the pull request
7.Click on "create pull request" to create the pull request

REVIEW A PULL REQUEST:
1.Navigate to the repository on GitHub and click on the pull request tab and select the pull request you wish to review
2.Examine the changes made in the "files changed" tab
3.Using the "conversation" tab add comments to specific lines of code or files if needed request modifications from the author by leaving comments
4.If the changes are satisfactory,click the "approve" button 
5.If approved, merge the pull requests into the main branch using the "merge pull request" button

GitHub Actions:

Explain what GitHub Actions are and how they can be used to automate workflows. Provide an example of a simple CI/CD pipeline using GitHub Actions.

GitHub Actions is a continuous integration and continuous deployment(CI/CD) platform that allows you to automate workflows for GitHub repositories.It enables you to define specific tasks such as building,testing and deployment pipeline,and automate them using a YAML files and a cloud-based platform to run these workflows.To automate workflows using GitHub actions one needs to:
1.Create a ' .github/workflows ' directory if it does not exist, in your repository 
2.Inside the directory create a YAML file
3.Define the workflow's triggers, tasks,and settings in the YAML file(push,pull_request,schedule)
4.To perform tasks, use GitHubs' Actions built-in actions such as checkout,run and deploy
5.To control the workflow's behaviour, use conditionals such as if,else,else if, statements
6.Use environment variables to store sensitive data such as credentials
7.Using GitHub Actions' built-in debugging tools to test and debug workflow 

name:CI/CD Pipeline

on:
  push:
       branches:
          -main

jobs:
  build-and-deploy:
  runs-on:windows-latest

   steps:
      -name: Checkout code
      uses:actions/checkout@v2

    -name: Set up Node.js
    uses: actions/setup-node@v3
    with:
        node-version:'16'

    -name: Install dependencies
    run: npm install

    -name: Build and test 
    run: |
        npm run build
        npm run test

    -name: Deploy to production
    run: npm run deploy  

Introduction to Visual Studio:
What is Visual Studio, and what are its key features? How does it differ from Visual Studio Code?

Visual Studio is a comprehensive integrated development environment where you can write,edit,debug, and build codde and then deploy your application.Visual Studio differs from Visual Studio Code as it is a comprehensive Integrated Development Environment designed for large scale, complex projects and enterprise-level applications.It is more complex and has a feature-rich interface with a steeper learning curve.Whereas,Visual Studio Code is a lightweight ,open-source code editor for smaller-scale projects and rapid development, it is more minimalist and elegant making it easier to learn and use.

Integrating GitHub with Visual Studio:
Describe the steps to integrate a GitHub repository with Visual Studio. How does this integration enhance the development workflow?

STEPS:
1.Install Visual Studio and Git and setup
2.Open Visual Studio and navigate to the extensions menu search for "GitHub" and install "GitHub extensions for Visual Studio"
3.Open your browser of choice,go onto github.com and Create or Sign in into your GitHub account and create a repository for your project
4.Copy the code url from GitHub(click on the green button written "code"> and navigate to local>copy code url)
5.Open Visual Studio and select "File">"Clone repository" and paste the url and choose where to clone it in your local directory
6.Configure the repository by opening the "Team Explorer"(View>Team Explorer) click on connect select "GitHub", enter GitHub credentials and connect to the chosen repository
7.To link the repository to the project right-click on the project and select ' Add>Existing Project' select cloned repository as the location
8.After making changes to the project files,commit those changes using the "Team Explorer" window 
9.Push changes using the "sync" button in the ' team explorer ' window
10.Pull changes by clicking on "pull"

Integrations can enhance development workflow in many ways such as,Managing code changes seamlessly,committing,pushing and pulling changes directly from Visual Studio reducing manual effort and human error.They facilitate collaboration with team members using pull requests,code reviews and communication and sharing of updates,  enhancing teamwork and productivity.It reduces switching between applications with GitHub functionality accessible within Visual Studio,it enables the accessing and managing  of GitHub projects,issues and pull requests directly within Visual Studio.

Debugging in Visual Studio:

Explain the debugging tools available in Visual Studio. How can developers use these tools to identify and fix issues in their code?

Developers can set breakpoints in code to pause execution at specific lines, allowing developers to inspect variables, examine call stack, and understand how code behaves at runtime.
Watch windows are essential for monitoring variable values and expressions during debugging providing immediate insights into data flow.
Viewing the call stack window is vital for tracing the sequence of method calls leading to the current execution point, supporting in understanding the program flow and diagnosing issues.
The Debugging Toolbar includes controls such as step into, step over and step out allowing accurate navigation through code execution and in-depth examination of code behaviour.

Collaborative Development using GitHub and Visual Studio:

Discuss how GitHub and Visual Studio can be used together to support collaborative development. Provide a real-world example of a project that benefits from this integration.

GitHub provides a cloud-based version control system, allowing many developers to work simultaneously on the same project without overriding each other's changes, while Visual Studio integrates with GitHub to allow developers to manage code locally.Developers can create pull requests in GitHub allowing them to be able to review, merge code changes, and discuss changes before they are merged back into the main branch, Visual Studio allows them to create and manage pull requests directly from the Integrated Development Environment,simplifying the code review process.GitHub's project management tools such as issues and project boards which can be used to manage projects, additionally Visual Studio's Team Explorer allows developers to access features directly from their development environment.

EXAMPLE:A team working together on a web application

They create a new GitHub repository for their project, including README, Code files, documentation, and a  license.The team then clones the repository, using Git, to their local machines and work on features or bug fixes in their separate branches.After making the changes they push and commit the changes to their forks on GitHub.Create pull requests for code reviews and discussions, once approved changes are merged into the main branch.The team sets up CI/CD pipelines for automatic build, test, and deployment.Use GitHub issues for bug tracking and task management.For code suggestions and solutions use GitHub Copilot Chat in Visual Studio.


REFERENCES:
github.com
learn.microsoft
visualstudio.microsoft.com
docs.github.com
w3schools.com
geeksforgeeks.org


Submission Guidelines:
Your answers should be well-structured, concise, and to the point.
Provide real-world examples or case studies wherever possible.
Cite any references or sources you use in your answers.
Submit your completed assignment by [due date].
