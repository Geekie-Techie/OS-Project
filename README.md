# File Integrity Monitor

## Overview

`FileIntegrityMonitor` is a Java application designed to monitor a specified directory for changes in file integrity using SHA-256 checksums. The application calculates and stores the checksums of files within a directory and continuously monitors for any modifications by comparing current checksums with previously recorded ones.

## Features

- **SHA-256 Checksum Calculation**: Computes a SHA-256 hash of files to ensure their integrity.
- **Directory Monitoring**: Periodically checks for changes in the directory and detects added or deleted files.
- **Change Detection**: Outputs changes detected in the directory, including files that have been added or removed.

## Getting Started

### Prerequisites

- Java Development Kit (JDK) 8 or later.

### Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/Geekie-Techie/OS-Project.git
   ```

2. **Navigate to the Project Directory**

   ```bash
   cd OS-Project
   ```

3.  **Compile the Code**

    ```bash
    javac FileIntegrityMonitor.java
    ```

4.  **Run the Application**

    ```bash
    java FileIntegrityMonitor
    ```

The application will start monitoring the directory specified in the code.


### Configuration

- **Directory to Monitor**: Set the `directoryToMonitor` variable to the path of the directory you wish to monitor.

  ```java
  private static final String directoryToMonitor = "/path/to/your/directory/";
  ```
  
- **Polling Interval**: Adjust the sleep interval in the `monitorDirectory` method to change the frequency of directory checks.

  ```java
  Thread.sleep(5000);
  ```