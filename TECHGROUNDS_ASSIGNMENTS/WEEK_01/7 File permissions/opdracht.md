# [7- File Permissions]

File Permissions uses symbols, but the symbols are simpler to understand. That's attractive to sysadmins that are new to standard Linux permissions.

Each access level has a symbol:

| **Access level** | **Symbol** | Number |
| ---------------- | ---------- | ------ |
| Read             | r          | 4      |
| Write            | w          | 2      |
| Execute          | x          | 1      |

Each identity has a symbol:

| **Identity** | **Symbol** |
| ------------ | ---------- |
| User         | u          |
| Group        | g          |
| Others       | o          |

There are also operators to manipulate the permissions:

| **Task**                 | **Operator** |
| ------------------------ | ------------ |
| Grant a level of access  | +            |
| Remove a level of access | -            |
| Set a level of access    | =            |

The general `chmod` command syntax is the same:

```plaintext
command permissions directory/file## Key-terms
```

- CHOWN

- CHGRP

- USERADD

- GROUPADD

- CHMOD

- 

- ```
  ls -l /path/to/file
  ```

- ```
  stat /path/to/file
  ```

- ```
  stat -c "%U %G" /path/to/file
  ```

Exercise:

- Create a text file.

- Make a long listing to view the file’s permissions. Who is the file’s owner and group? What kind of permissions does the file have?

- Make the file executable by adding the execute permission (x).

- Remove the read and write permissions (rw) from the file for the group and everyone else, but not for the owner. Can you still read it?

- Change the owner of the file to a different user. If everything went well, you shouldn’t be able to read the file unless you assume root privileges with ‘sudo’.

- Change the group ownership of the file to a different group.

### Gebruikte bronnen

- [command line - How do file permissions work? - Ask Ubuntu](https://askubuntu.com/questions/83/how-do-file-permissions-work)
  [system - Where are passwords saved? - Ask Ubuntu

- https://www.redhat.com/sysadmin/manage-permissions

       How to manage Linux permissions for users, groups, and others

- [linux - How do I change the group ownership of a file in Ubuntu? - Stack Overflow](https://stackoverflow.com/questions/21865940/how-do-i-change-the-group-ownership-of-a-file-in-ubuntu)]
  https://stackoverflow.com/questions/21865940/how-do-i-change-the-group-ownership-of-a-file-in-ubuntu
- [How To List Users and Groups on Linux &ndash; devconnected](https://devconnected.com/how-to-list-users-and-groups-on-linux/)
- 

### Ervaren problemen

### Resultaat

![file&permission.png](file&permission.png)
