# [CRON JOBS]

In Ubuntu (and other Unix-like operating systems), a cronjob is a scheduled task that runs at specified intervals. These tasks are managed by a utility called cron, which runs in the background and executes commands or scripts according to a predefined schedule.

A cronjob is defined by a cron expression, which consists of five fields:

Minute (0-59)
Hour (0-23)
Day of the month (1-31)
Month (1-12 or names)
Day of the week (0-7 or names, where 0 and 7 represent Sunday)
Each field can contain a single value, a comma-separated list of values, a range of values (specified using a hyphen), or an asterisk (*) to indicate "every" value. Additionally, you can use special characters such as slashes (/) to specify intervals.

Here's an example of a cron expression:

javascript
Copy code

* * * * * /path/to/your/script.sh
          This expression indicates that the script located at /path/to/your/script.sh will be executed every minute, as each field is set to * (every possible value).

Cronjobs are typically managed using the crontab command, which allows users to view, edit, and remove their scheduled tasks. Each user on the system can have their own crontab file, which contains their individual scheduled tasks. Additionally, system-wide cronjobs can be defined in /etc/crontab and in the /etc/cron.d/ directory.

Cronjobs are commonly used for tasks such as:

Regular backups
System maintenance tasks (e.g., cleaning up temporary files)
Running periodic scripts (e.g., fetching updates, generating reports)
Monitoring system health
Overall, cronjobs are a convenient way to automate repetitive tasks on Unix-like systems like Ubuntu.

## Key-terms

[Schrijf hier een lijst met belangrijke termen met eventueel een korte uitleg.]

## Opdracht

Exercise:

- Create a Bash script that writes the current date and time to a file in your home directory.

- Register the script in your crontab so that it runs every minute.

- Create a script that writes available disk space to a log file in ‘/var/logs’. Use a cron job so that it runs weekly.

### Gebruikte bronnen

https://phoenixnap.com/kb/set-up-cron-job-linux

[How to Run Cron Jobs Every 5, 10, or 15 Minutes | Linuxize](https://linuxize.com/post/cron-jobs-every-5-10-15-minutes/)

### Ervaren problemen

[Geef een korte beschrijving van de problemen waar je tegenaan bent gelopen met je gevonden oplossing.]

### Resultaat

Exercise:

- Create a Bash script that writes the current date and time to a file in your home directory.
  
  

- Register the script in your crontab so that it runs every minute.
  
  

- Create a script that writes available disk space to a log file in ‘/var/logs’. Use a cron job so that it runs weekly.
  
  
