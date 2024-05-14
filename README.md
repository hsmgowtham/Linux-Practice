# Linux Operating System
1. **Linux Operating System**: It's like Unix and runs on the Linux Kernel.
2. **Linux Kernel**: It's the brain of Linux, handling how the computer works with its hardware.
3. **Linux Distributions**: They're full operating systems made by adding software to the Linux Kernel. They make sure everything runs smoothly.
4. **Software Packages and Utilities**: These are the added bits to the Linux Kernel to make it a full operating system.
5. **Flavors**: Linux comes in different types to fit different needs and likes of users.

## Linux Architecture
Hardware > Kernel > Shell > Applications

## Advantages
1. **Open-Source**: Anyone can access, modify, and distribute its code freely.
2. **Security**: It's more secure than other systems, with fewer vulnerabilities and less need for antivirus software.
3. **Easy Updates**: Software updates are frequent and simple to install.
4. **Choice of Distributions**: Many versions are available to suit different needs and preferences.
5. **Free to Use**: Linux can be downloaded and used for free.
6. **Community Support**: There's a large community to help with any issues or questions.
7. **Stability**: It rarely slows down or crashes, needing fewer reboots.
8. **Privacy**: It respects user privacy.
9. **High Performance**: It handles multiple tasks efficiently.
10. **Network-Friendly**: It's well-suited for networking.
11. **Flexibility**: You can install only the components you need.
12. **File Format Compatibility**: It works with many file formats.
13. **Easy Installation**: Quick and simple to install, even on older hardware.
14. **Efficient with Limited Space**: It functions well even with limited disk space.

## Unix and Linux Difference

**Unix:**
- Unix is an operating system developed by AT&T and its partners.
- It's known for its stability, security, and multi-user capabilities.
- Unix typically has proprietary licenses, meaning users may need to pay for its use.
- It's often found in enterprise environments and used in web servers, workstations, and PCs.
- Unix systems have various versions (variants) like macOS, Solaris, AIX, and HP-UX.

**Linux:**
- Linux is an open-source operating system developed by Linus Torvalds in 1991.
- It's based on the Linux kernel and inspired by Unix principles.
- Linux is freely available and can be modified and distributed by anyone.
- It's highly customizable and comes in many distributions (distros) like Ubuntu, Fedora, Debian, and CentOS.
- Linux is widely used in servers, personal computers, mobile devices, and embedded systems.

# Linux Commands
## Basics

1. **ls (list)**
   - Explanation: Lists files and directories in the current directory.
   - Example: 
     ```
     ls
     ```

2. **man (manual)**
   - Explanation: Displays the manual pages for a command.
   - Example: 
     ```
     man ls
     ```

3. **info**
   - Explanation: Provides information and documentation for commands.
   - Example: 
     ```
     info ls
     ```

4. **apropos (search)**
   - Explanation: Searches the manual pages for a specified keyword.
   - Example: 
     ```
     apropos search
     ```

5. **mv (move)**
   - Explanation: Moves or renames files.
   - Example: 
     ```
     mv oldname newname
     ```
     - Renaming a file:
       ```
       mv oldname newname
       ```
     - Using `-i` option to prompt before overwrite:
       ```
       mv -i oldname newname
       ```
     - Moving multiple files to a directory:
       ```
       mv file1 file2 file3 ~/stuff
       ```
     - Moving files to an existing directory:
       ```
       mv file1 file2 ~/existing_directory/
       ```

6. **mkdir (make directory)**
   - Explanation: Creates a new directory.
   - Example: 
     ```
     mkdir practice
     ```
     - Creating a directory:
       ```
       mkdir practice
       ```
     - Creating nested directories (and their parents if needed):
       ```
       mkdir -p ~/foo/bar
       ```

7. **cd (change directory)**
   - Explanation: Changes the current working directory.
   - Example: 
     ```
     cd practice
     ```
     - Changing to a directory:
       ```
       cd practice
       ```
     - Moving to the parent directory:
       ```
       cd ..
       ```

8. **rmdir (remove directory)**
   - Explanation: Removes an empty directory.
   - Example: 
     ```
     rmdir practice
     ```
     - Removing an empty directory:
       ```
       rmdir practice
       ```

9. **rm (remove)**
   - Explanation: Removes files or directories.
   - Example: 
     ```
     rm file1 file2
     ```
     - Removing multiple files:
       ```
       rm file1 file2 file3
       ```
     - Removing a directory and its contents recursively:
       ```
       rm -R directory/
       ```

10. **cat (concatenate)**
    - Explanation: Displays the contents of a file.
    - Example: 
      ```
      cat myfile.txt
      ```
      - Displaying the contents of a file:
        ```
        cat myfile.txt
        ```

11. **less**
    - Explanation: Displays the contents of a file, allowing scrolling.
    - Example: 
      ```
      less myfile.txt
      ```
      - Viewing contents of a file with less:
        ```
        less myfile.txt
        ```

12. **pwd (print working directory)**
    - Explanation: Prints the current working directory.
    - Example: 
      ```
      pwd
      ```
      - Printing the current working directory:
        ```
        pwd
        ```

13. **cal (calendar)**
    - Explanation: Displays the calendar for a specified month or year.
    - Example: 
      ```
      cal
      ```
      - Displaying the calendar of the current month:
        ```
        cal
        ```
      - Displaying the calendar of a specific year:
        ```
        cal 2021
        ```

14. **date**
    - Explanation: Prints the current date and time.
    - Example: 
      ```
      date
      ```
      - Displaying the current date and time:
        ```
        date
        ```

## Daily

1. **Clear the Terminal**:
   - Explanation: Clears the terminal screen, removing all previous commands and output.
   - Example: Press `Ctrl + l` or use the `clear` command.

2. **Run Command and Return to Directory**:
   - Explanation: Executes a command and then returns to the current directory.
   - Example: 
     ```
     (cd /home/user/Downloads/ && ls -l)
     ```
     - This command lists the contents of the Downloads directory and then returns to the current directory.

3. **Shortcut to Directories**:
   - Explanation: Creates shortcuts to frequently accessed directories using the `CDPATH` environment variable.
   - Example: 
     ```
     export CDPATH=$CDPATH:/var/www/
     cd html
     ```
     - Adds `/var/www/` to the `CDPATH` and then navigates to the `html` directory using `cd`.

4. **Replacing Words or Characters**:
   - Explanation: Replaces words or characters in a text file using the `sed` command.
   - Example: 
     ```
     sed 's/version/story/g' myfile.txt
     ```
     - Replaces every instance of "version" with "story" in the file `myfile.txt`.

5. **Cursor Movement Control**:
   - Explanation: Provides shortcuts for cursor movement and text modification in the terminal.
   - Examples:
     - `Ctrl-a`: Moves cursor to the start of a line.
     - `Ctrl-e`: Moves cursor to the end of a line.
     - `Ctrl-w`: Deletes the whole word to the left of the cursor.
     - `Ctrl-k`: Erases to the end of the line.
     - `Ctrl-u`: Erases to the beginning of the line.

6. **Run `top` in Batch Mode**:
   - Explanation: Runs the `top` command in batch mode for a specified period without user interaction.
   - Example: 
     ```
     top -b -d 10 -n 3 >> top-file
     ```
     - Runs `top` every 10 seconds for a total of 3 iterations and appends the output to a file called `top-file`.

7. **Duplicate Pipe Content with `tee`**:
   - Explanation: Duplicates the output of a command and writes it to multiple files using the `tee` command.
   - Example: 
     ```
     ps | tee file1 file2 file3
     ```
     - Sends the output of the `ps` command to three different files (`file1`, `file2`, and `file3`).

8. **`export` Command**:
   - Explanation: Marks environment variables to be exported with newly forked child processes.
   - Example: 
     ```
     export VARIABLE=value
     ```
     - Sets the environment variable `VARIABLE` to `value` and exports it to child processes.

9. **`basename` Command**:
   - Explanation: Strips directory and suffix from filenames.
   - Example: 
     ```
     basename test/gfg.txt
     ```
     - Prints `gfg.txt`, stripping the directory `test/`.