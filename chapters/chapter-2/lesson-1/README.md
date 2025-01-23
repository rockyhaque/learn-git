# Creating a Git Repository

A **Git repository** (or "repo") represents a single project. You'll typically have one repository for each project you work on. A repo is essentially just a directory that contains a project (other directories and files). The only difference is that it also contains a hidden `.git` directory. That hidden directory is where Git stores all of its internal tracking and versioning information for the project.

---

## Steps to Create a Git Repository

1. **Navigate to Your Desired Location:**  
   Open a terminal and navigate to the location where you want to store your project. For example:

   ```bash
   cd /path/to/your/project
   ```

2. **Create a Project Directory:**  
   Create a new directory for your project:

   ```bash
   mkdir webflyx
   cd webflyx
   ```

3. **Initialize the Git Repository:**  
   Run the following command to initialize a new Git repository:

   ```bash
   git init
   ```

   This creates a hidden `.git` directory inside your project folder, marking it as a Git repository.

4. **Verify the Repository:**  
   To confirm that the repository was created successfully, list the contents of the directory (including hidden files):

   ```bash
   ls -a
   ```

   You should see the `.git` directory listed.

---

## Example: Creating a Repository for "WebFlyx"

In this example, we'll create a Git repository for **WebFlyx**, an imaginary self-hosted video streaming application.

1. Navigate to your desired location:

   ```bash
   cd /path/to/your/projects
   ```

2. Create a directory for WebFlyx:

   ```bash
   mkdir webflyx
   cd webflyx
   ```

3. Initialize the Git repository:

   ```bash
   git init
   ```

4. Verify the repository:

   ```bash
   ls -a
   ```

   You should see the `.git` directory, confirming that your repository has been created successfully.

---

Happy coding! 🚀
