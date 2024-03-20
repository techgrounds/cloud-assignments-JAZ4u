# [CRON JOBS]

In Ubuntu (and other Unix-like operating systems), a cronjob is a scheduled task that runs at specified intervals. These tasks are managed by a utility called cron, which runs in the background and executes commands or scripts according to a predefined schedule.

A cronjob is defined by a cron expression, which consists of five fields `` * * * * *``  :

First `*` = Minute (0-59)
Second `*`= Hour (0-23)
Third `*`= Day of the month (1-31)
Fourth `*`= Month (1-12 or names)
Fifth `*`= Day of the week (0-7 or names, where 0 and 7 represent Sunday)
Each field can contain a single value, a comma-separated list of values, a range of values (specified using a hyphen(`-`)), or an asterisk (`*`) to indicate "every" value. Additionally, you can use special characters such as slashes (`/`) to specify intervals.

| `*`        | Time Value       | (Range)                                        |
| ---------- | ---------------- | ---------------------------------------------- |
| First `*`  | Minute           | (0-59)                                         |
| Second `*` | Hour             | (0-23)                                         |
| Third `*`  | Day of the Month | (1-31)                                         |
| Fourth `*` | Month            | (1-12 or names)                                |
| Fifth `*`  | Day of the Week  | (0-7 or names, where 0 and 7 represent Sunday) |

Here's an example of a cron expression:

```
* * * * * /path/to/your/script.sh
```

   This expression indicates that the script located at ```/path/to/your/script.sh``` will be executed every minute, as each field is set to ``*`` (`*`   = every possible value).

Cronjobs are typically managed using the ``` crontab -e``` command, which allows users to view, edit, and remove their scheduled tasks. Each user on the system can have their own crontab file, which contains their individual scheduled tasks. Additionally, system-wide cronjobs can be defined in /etc/crontab and in the /etc/cron.d/ directory.

Cronjobs are commonly used for tasks such as:

Regular backups
System maintenance tasks (e.g., cleaning up temporary files)
Running periodic scripts (e.g., fetching updates, generating reports)
Monitoring system health.

Overall, cronjobs are a convenient way to automate repetitive tasks on Unix-like systems like Ubuntu.

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Opdracht

**Exercise:**

- Create a Bash script that writes the current date and time to a file in your home directory.

- Register the script in your crontab so that it runs every minute.

- Create a script that writes available disk space to a log file in ‘/var/logs’. Use a cron job so that it runs weekly.

### Gebruikte bronnen

https://phoenixnap.com/kb/set-up-cron-job-linux

[How to Run Cron Jobs Every 5, 10, or 15 Minutes | Linuxize](https://linuxize.com/post/cron-jobs-every-5-10-15-minutes/)

CHAT_GPT  

### Ervaren problemen

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Resultaat

**Exercise:**

- Create a Bash script that writes the current date and time to a file in your home directory.

- Register the script in your crontab so that it runs every minute.

- Create a script that writes available disk space to a log file in ‘/var/logs’. Use a cron job so that it runs weekly.

Here's a script that retrieves the available disk space and writes it to a log file in ``/var/log``. We named this script `disk_space_logger.sh` :

```
touch /scripts/disk_space_logger.sh
```

```
#!/bin/bash

# Define log file path

log_file="/var/log/disk_space.log"

# Get current date and time

current_date=$(date +"%Y-%m-%d %H:%M:%S")

# Get available disk space and append it to log file

df -h >> "$log_file"

# Add a timestamp to the log entry

echo "Disk space checked at $current_date" >> "$log_file"

echo "Disk space logged at $log_file"
```

![cron_job_3_script.png](cron_job_3_script.png)


Save this script with the name ``disk_space_logger.sh`` and make it executable using `chmod +x disk_space_logger.sh `

Next, we'll set up a cron job to run this script weekly. To do this, follow these steps:

-Open  crontab file for editing by running:

```
crontab -e
```

-Add the following line to the crontab file to schedule the script to run weekly:

```
0 0 * * 0 /path/to/disk_space_logger.sh
```

This line will run the script at midnight (00:00) every Sunday (day of the week 0).

-Replace`/path/to/disk_space_logger.sh` with the <u>actual</u> path to your `disk_space_logger.sh` script.

-Save and close the crontab file.

With this setup, your script will run weekly, logging the available disk space to the specified log file in `/var/log/disk_space.log`

![cron_job_3.png](cron_job_3.png)
