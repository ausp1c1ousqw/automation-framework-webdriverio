# Automation Framework

A modular web automation framework built with Node.js and ES modules. Designed to simplify web testing by providing reusable components for page objects, web elements, logging, and debugging.

## Features

- **Modular Design** – Organized into GUI, Utils, Helpers, and Logger modules.
- **Page Object Support** – Base classes and common elements to model web pages efficiently.
- **Logging** – Built-in Winston logger for test-specific and process-level logging.
- **Debugging Helpers** – Utilities for taking screenshots and saving page sources.
- **File Utilities** – Functions for managing directories and generating timestamped files.

## Modules

### GUI Module

Provides the core classes for interacting with web pages.

- **BasePage** – Common page actions like `open()`, `refresh()`, `back()`, `forward()`.
- **BaseElement** – Base class for all web elements.
- **Elements** – Includes `Button`, `Input`, `Checkbox`, `Label`, `Link`, `Dropdown`, `Frame`.
- **Utils** – Functions like `assertWithLogging`, `navigateTo`, `waitUntil`.

### Utils Module

Functions to manage files, directories, and timestamps:

- `ensureDirExists` – Makes sure a directory exists.
- `generateTimestampedFileName` – Creates unique filenames with timestamps.
- `getDailyDebugDir` – Returns the directory for daily debug files.

### Helpers Module

Assistive functions for debugging and capturing test artifacts:

- `getAndSavePageSource` – Saves the current page source to a file.
- `takeAndSaveScreenshot` – Captures and saves a screenshot.

### Logger Module

Logging utilities built with Winston:

- `logger` – Main logger instance.
- `startLoggingForTest` / `stopLoggingForTest` – Manage per-test log files.
- `subscribeLoggerToProcessEvents` – Logs uncaught exceptions and process events.
