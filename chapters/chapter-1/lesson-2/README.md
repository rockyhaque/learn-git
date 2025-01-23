# Install Git

Git is a powerful **command-line tool** used for version control. Whether you're a beginner or an experienced developer, installing Git is the first step to managing your code effectively. This guide will help you install Git on your system and verify that it's ready to use.

---

## Check if Git is Already Installed

Before installing Git, check if it's already installed on your system. Open a terminal and run the following command:

```bash
git --version
```

- If you see a version number (e.g., `git version 2.39.2`), Git is already installed, and you're good to go!
- If Git is not installed, you'll need to install it using the instructions below.

---

## Installation Instructions

### **Windows (WSL) / Linux (Ubuntu)**

1. Open a terminal.
2. Run the following command to install Git:

   ```bash
   sudo apt install git-all
   ```

3. Once the installation is complete, verify it by running:

   ```bash
   git --version
   ```

---

### **macOS**

#### Option 1: Using the Default Prompt

1. Open a terminal.
2. Run the following command:

   ```bash
   git --version
   ```

   - If Git is not installed, macOS will prompt you to install it. Follow the on-screen instructions.

#### Option 2: Using Homebrew

1. If you have Homebrew installed, run the following command:

   ```bash
   brew install git
   ```

2. Verify the installation:

   ```bash
   git --version
   ```

#### Option 3: Using Xcode

1. Install **Xcode** from the App Store (if you don't already have it).
2. Open a terminal and run:

   ```bash
   xcode-select --install
   ```

   This will install the **Command Line Tools** package, which includes Git.

3. Verify the installation:

   ```bash
   git --version
   ```

---

## Verify Installation

After installing Git, verify that it's working correctly by running:

```bash
git --version
```

You should see the installed version of Git displayed in the terminal.

---

## Next Steps

Now that Git is installed, you're ready to start using it! Explore the next chapters to learn how to create repositories, track changes, and collaborate with others using Git.

Happy coding! 🚀
