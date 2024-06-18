[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-22041afd0340ce965d47ae6ef1cefeee28c7c493a6346c4f15d667ab976d596c.svg)](https://classroom.github.com/a/vbnbTt5m)
[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15293110&assignment_repo_type=AssignmentRepo)
# Dev_Setup
Setup Development Environment

#Assignment: Setting Up Your Developer Environment

#Objective:
This assignment aims to familiarize you with the tools and configurations necessary to set up an efficient developer environment for software engineering projects. Completing this assignment will give you the skills required to set up a robust and productive workspace conducive to coding, debugging, version control, and collaboration.

#Tasks:

1. Select Your Operating System (OS):
   Choose an operating system that best suits your preferences and project requirements. Download and Install Windows 11. https://www.microsoft.com/software-download/windows11

Connect the USB flash drive to your technician PC.
Open Disk Management: Right-click on Start and choose Disk Management.
Format the partition: Right-click the USB drive partition and choose Format. Select the FAT32 file system to be able to boot either BIOS-based or UEFI-based PCs.
Set the partition as active: Right-click the USB drive partition and click Mark Partition as Active.

Step 2 - Copy Windows Setup to the USB flash drive.

Use File Explorer to copy and paste the entire contents of the Windows product DVD or ISO to the USB flash drive.
Optional: add an unattend file to automate the installation process. For more information, see Automate Windows Setup.


Connect the USB flash drive to a new PC.
Turn on the PC and press the key that opens the boot-device selection menu for the computer, such as the Esc/F10/F12 keys. Select the option that boots the PC from the USB flash drive.
Windows Setup starts. Follow the instructions to install Windows.
Remove the USB flash drive.

also update drivers


2. Install a Text Editor or Integrated Development Environment (IDE):
   Select and install a text editor or IDE suitable for your programming languages and workflow. Download and Install Visual Studio Code. https://code.visualstudio.com/Download

   look for your operating system then click either Ubuntu or Windows
Look for the installer vscode usersetup

By default, VS Code is installed under C:\Users\{Username}\AppData\Local\Programs\Microsoft VS Code.

Another way is ti download a zIP archive and extract it and run Code from there
  Setup will add Visual Studio Code to your %PATH%, so from the console you can type 'code .' to open VS Code on that folder. You will need to restart your console after the installation for the change to the %PATH% environmental variable to take effect.
 https://code.visualstudio.com/docs/?dv=win64user
 Click  I agree
 then launch vscode

3. Set Up Version Control System:
   Install Git and configure it on your local machine. Create a GitHub account for hosting your repositories. Initialize a Git repository for your project and make your first commit. https://github.com

   -Download Git 
   -select your Operating System
   Run installer
   "Use Git from Windows Command
   After installling Git 
   open from desktop or desktop shortcut
   Set your uSername and email git config username "Your name
   ".
   Git config-- global user.email "your email"
   Create a Github Accout
   Sign up for GitHub
   Create a new project  mkdir my-project
   Initialize new Git repository type git init
   then type git add (Filenme)
   Add Remote Repository git remote add origin https://github.com/your-username/my-project.git.
   Then git push -uorigin master

4. Install Necessary Programming Languages and Runtimes:
  Instal Python from http://wwww.python.org programming language required for your project and install their respective compilers, interpreters, or runtimes. Ensure you have the necessary tools to build and execute your code.

5. Install Package Managers:
   If applicable, install package managers like pip (Python).

Install Python:

Download the latest version of Python from the official Python website.
Run the installer and make sure to check the option "Add Python to PATH".
Follow the installation prompts.
Verify Python and pip Installation:

Open Command Prompt (search for "cmd" in the Start menu).
Type the following commands to verify the installation:
sh
Copy code
python --version
pip --version
You should see the installed versions of Python and pip.
Upgrade pip (Optional):

It’s a good idea to upgrade pip to the latest version:
sh
Copy code
python -m pip install --upgrade pip

6. Configure a Database (MySQL):
   Download and install MySQL database. https://dev.mysql.com/downloads/windows/installer/5.7.html

   After clicking the link Go to download section then scroll down download Mysql community select.
   You will look for Mysql installer then select then on Archives choose 5.7 click download choose the second as it has all packages.Activate the installer when finishing downloading.
   You will enter into  Mysql installer  choose the custom but you can choose any you like.Click Next .
   On Check requirements, execute all it will also download vs installer,choose all click next.
   Installation it will install all the things such as SQL shell,workbench for like 20 minutes.
   Product Configuration click Next.
   Type and Networking let it as default tick advanced and logging.
   accounts and roles, it will ask you to create a password for your Local mysql.Also you can add user then assign user.
   Logging options click general log ,path mysql log.Click next.
   Advanced Id Leave it as default Server id 1 and Lowercase.
   Click finish 
   Product Configuration click on Next.
   To connect to server, your passowrd  will be asked.
   Apply configuartion -it will check for scripts.Click next .
   Installation complete click finish.
   then it will start Mysql you will enter your password.
   to create a database click datbase, create database  it will ask you hostname put sever local address.

7. Set Up Development Environments and Virtualization (Optional):
   Consider using virtualization tools like Docker or virtual machines to isolate project dependencies and ensure consistent environments across different machines.
   Step 1: Install Docker
Download Docker Desktop:

Go to Docker Desktop.
Download the installer for your operating system (Windows, macOS, or Linux).
Install Docker Desktop:

Run the downloaded installer and follow the installation prompts.
After installation, Docker Desktop will require a restart of your computer.
Verify Installation:

Open a terminal (Command Prompt, PowerShell, or Git Bash).
Run the following command to verify that Docker is installed correctly:
bash
Copy code
docker --version
Step 2: Create a Dockerfile
Create a Dockerfile:

In your project directory, create a file named Dockerfile (without an extension).
Add the following basic content to your Dockerfile for a Python project:
Dockerfile
Copy code
# Use the official Python image from the Docker Hub
FROM python:3.8-slim

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

 Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

 Make port 80 available to the world outside this container
EXPOSE 80

#Define environment variable
ENV NAME World

#Run app.py when the container launches
CMD ["python", "app.py"]
Create a requirements.txt File:

This file should list all the Python packages your project depends on. Example:
plaintext
Copy code
flask
requests
Build the Docker Image:

Open a terminal in your project directory and run:
bash
Copy code
docker build -t my-python-app .
Run the Docker Container:


8. Explore Extensions and Plugins:
   Explore available extensions, plugins, and add-ons for your chosen text editor or IDE to enhance functionality, such as syntax highlighting, linting, code formatting, and version control integration.

9. Document Your Setup:
    Create a comprehensive document outlining the steps you've taken to set up your developer environment. Include any configurations, customizations, or troubleshooting steps encountered during the process. 

#Deliverables:
- Document detailing the setup process with step-by-step instructions and screenshots where necessary.
- A GitHub repository containing a sample project initialized with Git and any necessary configuration files (e.g., .gitignore).
- A reflection on the challenges faced during setup and strategies employed to overcome them.

#Submission:
Submit your document and GitHub repository link through the designated platform or email to the instructor by the specified deadline.

#Evaluation Criteria:**
- Completeness and accuracy of setup documentation.
- Effectiveness of version control implementation.
- Appropriateness of tools selected for the project requirements.
- Clarity of reflection on challenges and solutions encountered.
- Adherence to submission guidelines and deadlines.

Note: Feel free to reach out for clarification or assistance with any aspect of the assignment.
