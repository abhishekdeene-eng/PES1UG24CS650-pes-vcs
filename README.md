# PES Version Control System (VCS) Project

## Overview

This project implements a simplified Git-like Version Control System (VCS) in C. It demonstrates core concepts of version control such as object storage, tree structures, staging (index), and commit history.

---

## Features

* Blob object storage using SHA-256 hashing
* Tree objects representing directory structure
* Index (staging area) for tracking file changes
* Commit system with parent linking
* Log functionality to display commit history

---

## Phase 1: Object Storage

In this phase, file contents are stored as blob objects. Each object is uniquely identified using a SHA-256 hash, ensuring data integrity and deduplication.

---

## Phase 2: Tree Structure

Tree objects are implemented to represent the directory structure. Each tree stores file metadata such as mode, filename, and object hash.

---

## Phase 3: Index (Staging Area)

The staging area tracks files that are prepared for the next commit. Functions implemented:

* `index_load`
* `index_save`
* `index_add`

---

## Phase 4: Commit System

The commit system creates snapshots of the project state. Each commit stores:

* Tree reference
* Parent commit (if exists)
* Author and timestamp
* Commit message

---

## Screenshots

All required screenshots are included in **report.pdf**.

---

## Analysis Questions

### Q5: Branching

**5.1 What is a branch?**
A branch is a pointer to a specific commit in the version control system. It allows developers to work independently on different features without affecting the main codebase.

**5.2 How are branches implemented in PES?**
Branches are implemented as files inside `.pes/refs/heads/`. Each branch file stores the hash of the latest commit. The `HEAD` file points to the current branch.

**5.3 How would you implement checkout?**
Checkout can be implemented by updating the `HEAD` pointer, restoring files from the selected commit’s tree, and updating the index accordingly.

---

### Q6: Garbage Collection

**6.1 Why is garbage collection needed?**
Garbage collection removes unused or unreachable objects, reducing storage usage and improving repository efficiency.

**6.2 How would you implement garbage collection?**
It can be implemented by traversing all reachable objects starting from `HEAD` and deleting any objects that are not referenced.

---

## Conclusion

This project provides a practical understanding of how version control systems like Git manage data efficiently. It covers object storage, indexing, and commit history, forming the foundation of modern version control systems.

---

## Repository Link

🔗 https://github.com/abhishekdeene-eng/PES1UG24CS650-pes-vcs
