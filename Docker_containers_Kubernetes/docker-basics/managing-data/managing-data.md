# Managing Data in Docker (Basics)

## Context

Before moving into volumes, it is important to understand how data is handled in Docker.

There are different types of data involved when working with:
- Images
- Containers
- Volumes (next topic)

---

## Types of Data

### 1. Application Data

This includes:
- Source code
- Dependencies / packages
- Environment setup

This data is usually provided by the developer or a third party and is added during the build process.

Once it is added to the image:
- It becomes part of the image
- It is fixed (images are read-only)

This means:
- You cannot change this data without rebuilding the image

---

### 2. Temporary Data

Example:
- User input
- Runtime-generated data

This type of data:
- Is created and used while the container is running
- Can change frequently (read + write)
- Is stored inside the container

However:
- It is temporary
- It is lost when the container is removed

---

### 3. Permanent Data

Examples:
- Files
- Databases
- Application state

This data:
- Must persist even if the container stops or restarts
- Is read + write
- Should not be tied to the container lifecycle

This is where Docker volumes become important.

---

## Key Takeaways

- Images are read-only and contain application setup
- Containers can store temporary data, but it is not persistent
- Permanent data should not live inside containers
- Volumes are used to handle persistent data (next topic)
