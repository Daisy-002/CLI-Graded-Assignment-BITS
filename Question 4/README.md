Question 4 - File Access and I/O Investigation

### Objective
The objective of this experiment was to investigate Linux file access and input/output (I/O) operations. The experiment involved identifying open file descriptors, demonstrating output and error redirection, observing system resource limits, and understanding how Linux manages file I/O.

# Execution and Observations
## Command 1
mkdir Question1

Observation
This command created a new directory named Question1 to store all files related to this task. Organizing files into separate directories improves project management.

## Command 2
cd Question1

Observation
This command changed the current working directory to Question1. All files created during this experiment were stored inside this directory.

## Command 3
touch Environment_Report.txt
touch README.md
mkdir screenshots

Observation
These commands created the main report tracking file, the documentation file, and a folder to safely archive the relevant screenshots of command executions.

## Command 4
ls -l /proc/$$/fd

Observation
This command displayed the file descriptors currently used by the shell process. It showed standard input (0), standard output (1), standard error (2), and the descriptor opened to manage the current interactive terminal loop.

## Command 5
echo "Linux I/O Investigation" > Environment_Report.txt

Observation
This command redirected standard output to the file Environment_Report.txt, initializing the report with default header text. The > operator overwrites the file if it already exists.

## Command 6
cat Environment_Report.txt

Observation
This command displayed the contents of Environment_Report.txt, confirming that the text was successfully written using standard output redirection.

## Command 7
ls > Environment_Report.txt

Observation
This command redirected the file system data directly into Environment_Report.txt instead of printing to the active terminal, showing how output redirection can be used to log directory states.

## Command 8
cat Environment_Report.txt

Observation
This command displayed the contents of Environment_Report.txt, confirming that the layout listing had been successfully redirected into the tracking file.

## Command 9
ls non_existing_file 2> error.txt

Observation
This command attempted to query a file that does not exist. The standard error message was redirected into error.txt using the 2> operator, isolating error streams from normal output.

## Command 10
cat error.txt

Observation
This command displayed the contents of error.txt, confirming that the diagnostic error message had been successfully redirected and saved into a distinct file.

## Command 11
ulimit -a

Observation
This command displayed the current operational resource limits of the shell process, including limits related to max open file handles, memory allocations, user process counts, and stack sizes.

## Command 12
cat Environment_Report.txt

Observation
This command displayed the compiled report. It verified that all required execution checks, command listings, and tracking logs had been recorded successfully.

Technical Observations
Linux assigns explicit numerical file descriptors to every running process for handling file stream inputs and outputs.

File descriptor 0 represents standard input (stdin).

File descriptor 1 represents standard output (stdout).

File descriptor 2 represents standard error (stderr).

Output redirection (>) captures standard run data into a file instead of displaying it on the active terminal view.

Error redirection (2>) isolates error messages independently, preventing diagnostic warnings from corrupting normal output logs.

Resource limits displayed by the ulimit utility regulate system resource consumption to maintain global operating system stability.

Conclusion
This experiment demonstrated how Linux manages file input/output workflows using file descriptors and redirection operators. Standard output and standard error can be controlled independently across distinct file destinations, facilitating modular logging and clean debugging processes. The ulimit command clearly exposed the current boundaries applied to process environments, showing how resource allocation maintains system security and stability.