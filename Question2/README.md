Question 2 - Secure Project Workspace Setup

Objective

The objective of this task was to create a secure project workspace, configure appropriate file permissions, verify ownership details, check the default umask value, and document how Linux permissions help protect project data.

Command 1

mkdir Question1

Observation

This command created a new directory named Question1 to store all the files related to Question 1. It helps organize the project files separately from other tasks.

Command 2

cd Question1

Observation

This command changed the current working directory to Question1. All subsequent files and directories for this task were created inside this folder.

Command 3

touch README.md

Observation

This command created an empty README.md file. It is used to document the commands executed and the observations made during the lab.

Command 4

mkdir -p ProjectWorkspace/{docs,src,backup}

Observation

This command created the main project workspace along with three subdirectories: docs, src, and backup. The -p option automatically creates the parent directory if it does not already exist.

Command 5

ls -R ProjectWorkspace

Observation

This command displayed the complete directory structure recursively. It confirmed that the required project directories were created successfully.

Command 6

echo "Directory Structure:" >> Project_Workspace_Report.txt
ls -R ProjectWorkspace >> Project_Workspace_Report.txt

Observation

These commands stored the directory structure inside the report file. The >> operator appends the output without deleting existing content.

Command 7

touch ProjectWorkspace/docs/project_plan.txt

Observation

This command created a sample project documentation file named project_plan.txt inside the docs directory.

Command 8

echo "Initial Project Documentation" > ProjectWorkspace/docs/project_plan.txt

Observation

This command added sample content to the project documentation file. The > operator writes the text into the file.

Command 9

ls -l ProjectWorkspace/docs/project_plan.txt

Observation

This command displayed the file permissions, ownership, and other details before modifying the permissions. It served as the baseline for comparison.

Command 10

chmod 600 ProjectWorkspace/docs/project_plan.txt

Observation

This command changed the file permissions to 600, allowing only the owner to read and write the file. All permissions for the group and others were removed.

Command 11

ls -l ProjectWorkspace/docs/project_plan.txt

Observation

This command verified that the permissions were successfully updated. The output changed from -rw-rw-r-- to -rw-------, confirming that only the owner has access.

Command 12

umask

Observation

This command displayed the current umask value of the system. The umask determines the default permissions assigned to newly created files and directories.

Command 13

cat Project_Workspace_Report.txt

Observation

This command displayed the contents of the report file. It confirmed that all required information, including directory structure, permissions, ownership details, umask value, and explanation, had been successfully recorded.

Conclusion

A secure project workspace was successfully created with separate folders for documentation, source code, and backups. File permissions were modified to restrict access to the owner only, ownership details were verified, the system's umask value was recorded, and the report documented how Linux permissions help secure sensitive project data.