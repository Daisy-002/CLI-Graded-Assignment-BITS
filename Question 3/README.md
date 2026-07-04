Question 3 - File System and Link Analysis

## Objective

The objective of this experiment was to understand the behavior of Linux hard links and symbolic links by creating both types of links, comparing their inode numbers, examining file metadata, and observing what happens after deleting the original file.

## Execution and Observations

### Command 1

mkdir Question1

#### Observation

This command created a new directory named Question1 to store all the files related to this task. It helps keep the assignment organized separately from other exercises.

### Command 2

cd Question1

#### Observation

This command changed the current working directory to Question1. All subsequent files and commands for this task were executed inside this directory.

### Command 3

touch Link_Analysis_Report.txt

#### Observation

This command created an empty report file named Link_Analysis_Report.txt. The report was later used to save the documented results of the link analysis experiment.

### Command 4

touch README.md

#### Observation

This command created a README.md file to document the commands executed and the observations made during the experiment.

### Command 5

echo "Linux Link Analysis Experiment" > original.txt

#### Observation

This command created the original file and stored sample content inside it. This file served as the primary source for creating both the hard and symbolic links.

### Command 6

ln original.txt hardlink.txt

#### Observation

This command created a hard link named hardlink.txt. A hard link shares the same underlying inode as the original file and directly points to the file's data block.

### Command 7

ln -s original.txt symlink.txt

#### Observation

This command created a symbolic link named symlink.txt. Unlike a hard link, a symbolic link functions as a shortcut, storing only the text pathname of the target file.

### Command 8

ls -li

#### Observation

This command displayed the inode numbers of all files. The output confirmed that original.txt and hardlink.txt shared the exact same inode number, while symlink.txt possessed a distinct inode.

### Command 9

stat original.txt hardlink.txt symlink.txt

#### Observation

This command displayed detailed file metadata, including specific inode numbers, permissions, link counts, ownership blocks, and timestamps, providing deep structural insight into each link type.

### Command 10

rm original.txt

#### Observation

This command deleted the original file. This step was performed to test and observe how the hard link and symbolic link independently behave once their source file is removed.

### Command 11

ls -li

#### Observation

This command listed the remaining directory contents after deleting the original file. The hard link continued to exist normally, whereas the symbolic link became broken, pointing to a missing target path.

### Command 12

cat hardlink.txt

#### Observation

This command successfully displayed the contents of the hard link. The underlying data remained fully readable because the data block persists as long as at least one hard link (inode reference) points to it.

### Command 13

cat symlink.txt

#### Observation

This command failed with an error because the symbolic link pointed to a text pathway that no longer existed, confirming that symbolic links depend entirely on the active presence of the original target filename.

### Command 14

cat Link_Analysis_Report.txt

#### Observation

This command displayed the completed report file. It confirmed that all essential verification details, including inode mappings, metadata checks, link behaviors, and final conclusions, were accurately saved.

## Summary of Findings

* The original file and hard link shared the exact same inode number.
* The symbolic link had a completely different inode because it only stores the text file path as its data.
* Deleting the original file had zero effect on the hard link's data availability.
* The symbolic link became unreadable and invalid immediately after the original file path was removed.
* This experiment clearly demonstrated the architectural distinction between physical file links and reference pointers in Linux.

## Conclusion

Hard links provide direct access to a file's raw data by sharing the exact same inode reference as the original target. Symbolic links simply reference a file's text pathname and instantly break if that path becomes invalid. This experiment highlights why hard links remain completely functional after the deletion of an original pointer name, while symbolic links do not.