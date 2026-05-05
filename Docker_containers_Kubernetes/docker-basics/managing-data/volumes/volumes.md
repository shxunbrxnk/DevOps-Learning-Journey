# Docker Volumes

## Introduction

Volumes are used to persist data in Docker applications.

They allow data to exist outside of a container so that it is not lost when the container stops or is removed.

---

## What is a Volume?

A volume is a directory on the host machine (hard drive) that is mounted into a container.

This means:
- A folder inside the container is linked to a folder outside the container
- Data can be shared between the container and the host machine

---

## Why Volumes are Needed

By default:
- Data inside a container is temporary
- If the container is deleted, the data is lost

Volumes solve this problem by storing data outside the container.

---

## Key Characteristics

- Volumes exist independently of containers
- If a container is removed, the volume still exists
- Containers can read and write data to volumes
- Multiple containers can use the same volume (in some cases)

---

## Simple Explanation

You can think of a volume as:

A shared folder between your local machine and a container.

---

## What this means in practice

- Your application can store data in a volume
- That data will still be there even if the container restarts
- This is important for things like:
  - databases
  - uploaded files
  - logs
