# Architecture Overview

This document outlines the high-level architecture of the Gemini Memory Bank framework.

## Core Components

1.  **Core Logic (`core/`)**: Contains the main dispatcher prompt (`main_prompt.md`) which analyzes user intent and loads context, and a set of best practices (`best_practices.md`).
2.  **Modes (`modes/`)**: A collection of Markdown files, each defining a specific operational mode for the AI.
3.  **Memory (`session_memory.md`)**: A long-term memory file that stores summaries of work sessions.
4.  **Manifest (`manifest.json`)**: A configuration file that registers all available modes and their metadata.
5.  **Documentation (`docs/`, `README.md`, `CHANGELOG.md`)**: Public-facing documentation for human developers.
