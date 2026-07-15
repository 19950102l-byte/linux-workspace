# Linux Workspace

> A professional desktop application for Linux server migration, backup, restore, deployment, and disaster recovery.

---

# Overview

Linux Workspace is a cross-platform desktop application designed to simplify Linux server migration and recovery.

Unlike traditional migration tools that only copy files, Linux Workspace is built around **Workspace**, **Package**, **Planning**, and **Restore** concepts.

The project focuses on:

- Safe migration
- Repeatable deployment
- Package-based recovery
- Dry Run planning
- Configuration validation
- History management
- Full event logging

The application runs entirely on the client side.

No server or agent is required.

---

# Project Goals

The primary goal is to build a professional Linux migration tool that is:

- Safe
- Visual
- Repeatable
- Extensible
- Easy to use

The project should support:

- Server migration
- Disaster recovery
- Configuration backup
- Environment cloning
- Multi-server deployment
- Repeatable restore

---

# Core Concepts

The project is built around several core concepts.

## Workspace

A Workspace represents an entire migration project.

It contains:

- Source server
- Packages
- Restore history
- Reports
- Logs
- Settings

---

## Package

A Package is generated from a Linux server.

It contains:

- Metadata
- Resources
- Configuration
- Validation information

Packages can be restored multiple times.

---

## Snapshot

Each package may contain multiple snapshots.

Snapshots allow version management.

Example:

Workspace

├── Snapshot V1

├── Snapshot V2

└── Snapshot V3

---

## Resource

Everything is treated as a Resource.

Examples:

- User
- Group
- Nginx Site
- SSL Certificate
- MySQL Database
- Cron Job
- System Service

Resources are the smallest recoverable unit.

---

## Restore Plan

Before recovery, Linux Workspace performs a Dry Run.

A Restore Plan is generated.

The Restore Engine only executes the Restore Plan.

---

# Features

Current roadmap includes:

- SSH Connection
- Package Generation
- Package Management
- Dry Run
- Restore Plan
- Conflict Resolution
- History
- Compare
- Validation
- Event Logging

---

# Architecture

Linux Workspace follows a layered architecture.

JavaFX UI

↓

Application Layer

↓

Workspace Engine

Package Engine

Planning Engine

Restore Engine

Compare Engine

History Engine

Validation Engine

↓

Infrastructure

SSH

SQLite

Scripts

Package Files

---

# Technology Stack

Frontend

- JavaFX

Language

- Java 21

Build

- Gradle

Database

- SQLite

Communication

- SSH
- SFTP

Compression

- tar
- zstd

Logging

- Logback

JSON

- Jackson

---

# Development Principles

This project follows several principles.

## Design First

No code before design.

Every feature must have:

- Specification
- Architecture
- Task
- Review

before implementation.

---

## Small Tasks

Each task implements one feature only.

Example:

TASK-001

Workspace

TASK-002

SQLite

TASK-003

SSH Connection

---

## Code Review Required

All code must be reviewed before merge.

---

## Dry Run First

Every restore operation must generate a Restore Plan.

No direct restore is allowed.

---

# Roadmap

## Phase 0

Project Design

- README
- Architecture
- Specifications
- UI
- Database

---

## Phase 1

Foundation

- Workspace
- SQLite
- SSH
- Package

---

## Phase 2

Migration

- Scanner
- Planning Engine
- Restore Engine

---

## Phase 3

Advanced Features

- Compare
- Dependency Analysis
- Plugin System

---

# Repository Structure

docs/

architecture/

database/

specifications/

tasks/

ui/

prototype/

src/

---

# License

Apache License 2.0

---

# Status

Current Status:

🚧 Designing Architecture

The project is currently under active design.

Implementation has not started yet.
