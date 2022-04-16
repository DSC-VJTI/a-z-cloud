---
title: "J"
linkTitle: "J"
weight: 4
description: >
  ## Job Scheduling
---

We often have repetitive tasks to perform such as checking internet connection every few hours, maybe checking stock prices every few hours, or checking if that one product has gone on sale on an e-commerce site. Instead of having to do this manually, you can _schedule_ these tasks to run at regular intervals.

For example, consider this `check_internet.sh` Bash script to check if you are connected to the internet or not by pinging Google's webpage:

```bash
echo -e "GET http://google.com HTTP/1.0\n\n" | nc google.com 80 > /dev/null 2>&1

if [ $? -eq 0 ]; then
    echo "Online"
else
    echo "Offline"
fi
```

Now, to run this script say, every 2 hours to check for internet connection, we use the `crontab` utility in Linux.

```bash
# enters the configuration file that contains cron jobs to be scheduled
crontab -e
# run this script every 2 hours
0 */2 * * *  check_internet.sh
```

Let's not get ahead of ourselves and first see what is a **cron job** and what does this terrible syntax `0 */2 * * *` mean.

### What is a cron job?

Derived from the Greek God of Time, Chronos, a cron job is a task that is scheduled by a job scheduler such as `crontab` on Linux-based operating systems and by `cron` on a Unix-like operating system.

To learn more about the uncommon asterisk syntax, refer [crontab.guru](https://crontab.guru/)

Though checking the internet connection is a trivial example, we have seen in [health checks]({{< relref "../H/_index.md" >}} "Health Checks") how important it is to check if a server or an application is healthy (alive) or not.

### Why do you need cloud for scheduling cron jobs?

From health checks to thousands of repetitive tasks such as fetching data from several APIs, to scheduling a job based on an event trigger, manually managing so many jobs becomes impossible. Hence, to manage jobs at scale, cloud is at our behest.

Job scheduling tools such as Google Cloud's Cloud Scheduler enable automation of execution of tasks based on date-time scheduling or other methods of execution such as event-based triggers. It eliminates the need for manual kick-offs, reducing delays and avoiding repetitive tasks.
