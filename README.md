# Eventually Consistent Distributed File System

Due to academic integrity, the project source code and detailed report are private. This public summary outlines the core objectives, challenges, and achievements. Code/reports cannot be shared, even on request.

## Project Overview

This project involved designing and implementing a simple distributed file system (DFS) using C++, gRPC, and Protocol Buffers. The system enables multiple clients to synchronize files with a central server, supporting both binary and text files.

## Problem Statement

The goal was to build a DFS that allows clients to upload, fetch, delete, and list files on a remote server, while ensuring eventual consistency across all clients. The system needed to handle concurrent operations, file versioning, and efficient file transfer, all while maintaining data integrity and supporting large files.

## High-Level Design

- **gRPC-based Communication:** All client-server interactions use gRPC with Protocol Buffers for efficient, language-agnostic messaging.
- **File Operations:** Implemented remote procedures for uploading, downloading, deleting, and listing files, as well as retrieving file metadata.
- **Streaming & Scalability:** Utilized gRPC streaming for large file transfers to avoid memory bottlenecks.
- **Consistency Model:** Achieved weak consistency using a combination of file watchers (to detect local changes) and server-driven callbacks (to notify clients of remote changes).
- **Concurrency & Synchronization:** Employed fine-grained locking and synchronization mechanisms to ensure safe concurrent access and updates.
- **Cross-Platform Support:** Designed to work with both binary and text files, supporting a variety of file sizes and types.

## Project Responsibilities

- Designed the protocol and message formats for all file operations using Protocol Buffers.
- Implemented both client and server logic in C++ using gRPC, including robust error handling and deadline management.
- Developed mechanisms for file versioning and conflict resolution based on modification timestamps.
- Integrated file system monitoring (using inotify) to detect and propagate local changes.
- Ensured thread-safe operations and efficient synchronization between multiple clients and the server.
- Wrote comprehensive documentation and performed extensive testing with edge cases (e.g., large files, concurrent modifications).

## Skills & Technologies Used

- C++14, gRPC, Protocol Buffers
- Multithreading, concurrency control, and synchronization primitives
- File system APIs and event monitoring (inotify)
- Network programming and distributed systems concepts
- Debugging, logging, and performance profiling

## Learning Outcomes

- Gained hands-on experience with distributed systems design and implementation.
- Developed a deep understanding of remote procedure calls, streaming, and consistency models.
- Improved skills in concurrent programming and cross-platform file handling.
- Practiced writing clear technical documentation and designing for maintainability.
