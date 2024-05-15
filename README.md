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

6. **mkdir (make directory)**
   - Explanation: Creates a new directory.
   - Example: 
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

11. **less**
    - Explanation: Displays the contents of a file, allowing scrolling.
    - Example: 
      ```
      less myfile.txt
      ```

12. **pwd (print working directory)**
    - Explanation: Prints the current working directory.
    - Example: 
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
Sure, here are the explanations and examples for the commands you mentioned, following a similar format:

10. **`chmod` Command**:
   - Explanation: Changes the permissions of files or directories in Linux.
   - Examples:
     ```
     chmod 755 file.txt
     ```
     - Grants read, write, and execute permission to the owner of `file.txt`, and read and execute permission to the group and others.
     The numbers used in the `chmod` command represent permissions in a numeric format. Each permission has a corresponding numeric value:

      - **4**: Read permission
      - **2**: Write permission
      - **1**: Execute permission

      These values are assigned to each of the three permission groups:

      1. **Owner**: The user who owns the file or directory.
      2. **Group**: The group associated with the file or directory.
      3. **Others**: Everyone else who is not the owner or in the group.

      To assign permissions using `chmod`, you add up the numeric values for the desired permissions:

      - **Read (r)**: 4
      - **Write (w)**: 2
      - **Execute (x)**: 1

      For example:

      - Read and write permission: 4 (read) + 2 (write) = 6
      - Read, write, and execute permission: 4 (read) + 2 (write) + 1 (execute) = 7
      - No permission: 0

      So, when you see a number like 755 in `chmod 755 file.txt`, it means:

      - The owner of the file (`7`) has read (4), write (2), and execute (1) permissions (4+2+1=7).
      - The group (`5`) has read (4) and execute (1) permissions (4+1=5).
      - Others (`5`) have read (4) and execute (1) permissions (4+1=5).

      This numeric representation provides a concise way to set permissions using `chmod` without having to spell out "read," "write," and "execute" each time.
     
     ```
     chmod u+x file.sh
     ```
     - Adds execute permission to the owner of `file.sh`.

11. **`chown` Command**:
   - Explanation: Changes the owner and/or group of a file or directory.
   - Examples:
     ```
     chown user1:group1 file.txt
     ```
     - Changes the owner of `file.txt` to `user1` and the group to `group1`.
     
     ```
     chown user2 file2.txt
     ```
     - Changes the owner of `file2.txt` to `user2` without changing the group.

12. **`grep` Command**:
   - Explanation: Searches text or files for specific patterns.
   - Examples:
     ```
     grep "pattern" file.txt
     ```
     - Searches `file.txt` for lines containing the specified "pattern" and prints them.
     
     ```
     grep -i "hello" *.txt
     ```
     - Searches for lines containing "hello" in all `.txt` files in the current directory, ignoring case.

13. **`find` Command**:
   - Explanation: Searches files and directories in a directory hierarchy based on various criteria.
   - Examples:
     ```
     find /home/user -type f -name "*.log"
     ```
     - Searches for all `.log` files in the `/home/user` directory.
     
     ```
     find . -type d -name "temp"
     ```
     - Searches for directories named "temp" in the current directory.