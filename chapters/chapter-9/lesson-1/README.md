# Git Remote

Often our frenemies (read: coworkers) make code changes that we need to begrudgingly accept into our pristine bug-free repos. /s

This is where the "distributed" in "distributed version control system" comes from. We can have "remotes," which are just external repos with mostly the same Git history as our local repo.

When it comes to Git (the CLI tool), there really isn’t a "central" repo. GitHub is just someone else’s repo. Only by convention and convenience have we, as developers, started to use GitHub as a "source of truth" for our code.

---

## Assignment

### Goal

Create a second repo called `webflyx-local` as a sibling directory to the original `webflyx` repo.

### Steps

1. **Navigate to the Parent Directory**

   ```bash
   cd path/to/parent/directory
   ```

2. **Create a New Repository**

   ```bash
   mkdir webflyx-local
   cd webflyx-local
   git init
   ```

3. **Verify Directory Structure**  
   After completing the steps, the directory structure should look like this:
   ```
   webflyx/
     - [stuff in the original repo]
   webflyx-local/
     - [stuff we’ll put in the new repo]
   ```

---

Done!
