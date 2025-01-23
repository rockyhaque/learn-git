# Chapter 3: Git Internals

In this chapter, you'll dive into the inner workings of Git, exploring how it stores and manages data under the hood. You'll learn about Git's object model, including commits, trees, and blobs, and how these components work together to create a powerful version control system. By the end of this chapter, you'll have a deeper understanding of Git's architecture and how it tracks changes in your projects.

---

## Table of Contents

- [Lesson 1: Different Hashes](./lesson-1/README.md)  
   Learn about Git's use of SHA-1 hashes to uniquely identify commits, trees, and blobs.

- [Lesson 2: The Plumbing](./lesson-2/README.md)  
   Explore Git's low-level (plumbing) commands and how they interact with the repository's internal data.

- [Lesson 3: The Object File](./lesson-3/README.md)  
   Understand how Git stores data as objects in the `.git` directory.

- [Lesson 4: Cat File](./lesson-4/README.md)  
   Use the `git cat-file` command to inspect the contents of Git objects.

- [Lesson 5: Trees and Blobs](./lesson-5/README.md)  
   Learn about Git's tree and blob objects, which represent directories and file contents, respectively.

- [Lesson 6: Second Commit](./lesson-6/README.md)  
   Explore how Git handles multiple commits and builds a history of changes.

- [Lesson 7: Storing Data](./lesson-7/README.md)  
   Understand how Git efficiently stores and compresses data to manage large repositories.

---

## Learning Objectives

By the end of this chapter, you'll:

1. Understand Git's object model and how it represents data.
2. Use low-level Git commands to inspect and manipulate repository data.
3. Explore the structure of Git objects, including commits, trees, and blobs.
4. Learn how Git builds and maintains a history of changes.
5. Gain insight into Git's data storage and compression mechanisms.

---

## Prerequisites

Basic familiarity with Git commands (e.g., `git init`, `git add`, `git commit`) and terminal usage is recommended. If you're new to Git, review Chapters 1 and 2 before starting this chapter.

---

## Start Your Journey

Begin with [Lesson 1: Different Hashes](./lesson-1/README.md) to learn how Git uses hashes to uniquely identify objects and build a robust version control system.

Happy coding! 🚀
