**Author:** &nbsp; Shilpak Deb

Implementation of a Peer to Peer Distributed File Sharing System

---

## Instructions for Execution:

The following are the steps for how to establish the P2P file sharing network:

- **STEP 1:** &nbsp; Navigate to inside the _P2P File Sharing System_ folder:

- **STEP 2:** &nbsp; Open multiple terminals via terminator (enter the following command)

```bash
terminator
```

- **STEP 3:** &nbsp; Split the terminal into multiple parts for running individual trackers/clients

- **STEP 4:** &nbsp; Following are the instructions to open a tracker or client:

### How to Start (Tracker):

For each terminal where you wish to start a tracker, type the following commands: ( **tracker_no** should be unique for each client )

```bash
cd ../tracker
make
./tracker tracker_info.txt tracker_no
```

### How to Start (Client):

For each terminal where you wish to start a client, type the following commands: ( **\<IP\>:\<PORT\>** should be unique for each tracker )

```bash
cd ../client
make
./client <IP>:<PORT> tracker_info.txt
```

---

## Folder Contents:

**( Folder Name**: P2P File Sharing System **)**

### tracker: (directory)

- **_makefile_**
  - Compiles the entire set of .cpp files inside **tracker** directory in one go and create the '**tracker**' executable file
- **_tracker.cpp_**
  - Contains the **main** function and definitions for external global variables
- **_commands.cpp_**
  - Contains individual functions for each of the commands to be implemented (at **tracker** end)
- **_misc.cpp_**
  - Contains some miscellaneous functions that are used multiple times throughout the program
- **_tracker.h_**
  - Allows the various functions and external global variables to be accessed from any of the .cpp files in **tracker** directory
- **_tracker_**
  - Executable file for **tracker** created via makefile

### client: (directory)

- **_makefile_**
  - Compiles the entire set of .cpp files inside **client** directory in one go and create the '**client**' executable file
- **_client.cpp_**
  - Contains the **main** function and definitions for external global variables
- **_commands.cpp_**
  - Contains individual functions for each of the commands to be implemented (at **client** end)
- **_comm.cpp_**
  - Contains funcitons to implement client-to-client communcations
- **_fileop.cpp_**
  - Contains functions to perform various file operations (reading from/writing to a file in chunks, calculating SHA1 hash for a chunk, etc.)
- **_misc.cpp_**
  - Contains some miscellaneous functions that are used multiple times throughout the program
- **_client.h_**
  - Allows the various functions and external global variables to be accessed from any of the .cpp files in **client** directory
- **_client_**
  - Executable file for **client** created via makefile

### tracker_info.txt

- Stores the IP and PORT of the the default and backup trackers
- ( **LINE 1:** Default Tracker )
- ( **LINE 2:** Backup Tracker )

### README.md

- README file for Assignment

---
