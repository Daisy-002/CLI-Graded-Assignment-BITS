## Question 5 - Storage Health Assessment and Documentation

### Objective
The objective of this experiment was to assess the storage resources available on the Linux system. Storage devices, mounted file systems, disk usage, inode utilization, and overall storage health were examined. The report was created using the text editor as required.

### Execution and Observations
## Command 1
mkdir Question1

Observation
This command created a new directory named Question1 to store all files related to this task. Keeping each exercise in a separate directory improves file management and organization.

## Command 2
cd Question1

Observation
This command changed the current working directory to Question1. All subsequent files and commands for this task were executed inside this directory.

## Command 3
touch README.md
mkdir screenshots

Observation
These commands created the standard documentation file (README.md) and a dedicated folder to securely store system screenshots taken during the experiment.

## Command 4
cat >> Environment_Report.txt

Observation
This command appended the storage investigation details directly into Environment_Report.txt, ensuring all environment parameters are recorded in a single cohesive log file as required.

## Command 5
df -h

Observation
This command displayed the available storage and disk utilization statistics in a human-readable format. It provided clear information regarding total device capacities, used space, and active mount configurations.

## Command 6
mount

Observation
This command displayed all mounted file systems currently initialized on the virtual instance. It exposed active mount points, file system types, and their respective operational read/write permissions.

## Command 7
df -h

Observation
This command analyzed disk usage statistics across the active filesystem array. It tracked absolute data consumption, available remaining block spaces, and percentage utilization metrics for each partition.

## Command 8
df -i

Observation
This command displayed structural inode usage statistics for the mounted file systems. Checking inode allocation ensures that the system has enough index nodes remaining to safely generate new file records.

## Command 9
cat Environment_Report.txt

Observation
This command displayed the completed environment tracking file. It verified that all essential storage metrics, device lists, block utilization percentages, and inode statuses were successfully captured.

### Storage Health Observations
The active file systems were completely responsive, properly mounted, and fully accessible.

Total block storage utilization and data footprint parameters remained well within stable operational thresholds.

Inode utilization tracking indicated robust capacity levels, leaving plenty of room for creating additional file indexes.

No storage-related bottlenecks or device failures were flagged during the environment evaluation.

### Recommendations
Periodically check active block usage logs to proactively prevent storage exhaustion events.

Clear transient log files and system caches regularly to preserve system volume integrity.

Archive stale build artifacts or historical datasets to reduce overall disk footprint.

Keep persistent automated backups of critical workspace tracking files.

Review inode availability alongside standard disk checks to safeguard against structural filesystem limits.

### Conclusion
This experiment demonstrated how Linux utilities supply deep observability into block storage resources and file system health. Core diagnostics like df -h and df -i give system operators immediate insights into data volume usage, partition maps, active mounts, and table structures. Routine tracking ensures high workspace reliability, predictable behavior, and efficient system administration.