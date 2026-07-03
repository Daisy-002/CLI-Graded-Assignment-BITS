# 🐧 Question 1 – Linux Environment Verification

This document describes the Linux commands executed to verify the system environment and generate the `Environment_Report.txt` file.

---

## 📌 Command 1

```bash
mkdir Question1
```

### 🔍 Observation

* Created a new directory named **Question1**.
* This directory stores all files related to **Question 1** of the assignment.

---

## 📌 Command 2

```bash
cd Question1
```

### 🔍 Observation

* Changed the current working directory to **Question1**.
* All subsequent commands and files were executed inside this directory.

---

## 📌 Command 3

```bash
pwd
```

### 🔍 Observation

* Displayed the absolute path of the current working directory.
* Confirmed that the terminal was inside the **Question1** directory.

---

## 📌 Command 4

```bash
whoami
```

### 🔍 Observation

* Displayed the username of the currently logged-in user (**daisy**).
* Verified the active Linux account.

---

## 📌 Command 5

```bash
echo "Username: $(whoami)" >> Environment_Report.txt
```

### 🔍 Observation

* Appended the username to **Environment_Report.txt**.
* The `>>` operator adds data without overwriting the existing file.

---

## 📌 Command 6

```bash
groups
```

### 🔍 Observation

* Displayed all groups associated with the current user.
* These groups determine the user's permissions and access rights.

---

## 📌 Command 7

```bash
echo "Groups: $(groups)" >> Environment_Report.txt
```

### 🔍 Observation

* Appended the group information to **Environment_Report.txt** for documentation.

---

## 📌 Command 8

```bash
echo $SHELL
```

### 🔍 Observation

* Displayed the current shell (`/bin/bash`).
* The shell is responsible for interpreting and executing Linux commands.

---

## 📌 Command 9

```bash
echo "Shell: $SHELL" >> Environment_Report.txt
```

### 🔍 Observation

* Saved the shell information into **Environment_Report.txt**.

---

## 📌 Command 10

```bash
pwd
```

### 🔍 Observation

* Displayed the current working directory again before recording it in the report.

---

## 📌 Command 11

```bash
echo "Current Directory: $(pwd)" >> Environment_Report.txt
```

### 🔍 Observation

* Appended the absolute path of the current working directory to **Environment_Report.txt**.

---

## 📌 Command 12

```bash
ls -la
```

### 🔍 Observation

* Listed all files and directories, including hidden files.
* Displayed detailed information such as:

  * File permissions
  * Ownership
  * File size
  * Last modification date

---

## 📌 Command 13

```bash
ping -c 4 google.com
```

### 🔍 Observation

* Tested network connectivity by sending four ICMP packets to **google.com**.
* Successful replies with **0% packet loss** confirmed that the internet connection was working correctly.

---

## 📌 Command 14

```bash
cat Environment_Report.txt
```

### 🔍 Observation

* Displayed the contents of **Environment_Report.txt**.
* Verified that all required system information had been successfully recorded.

---

# ✅ Outcome

The Linux environment was successfully verified by:

* ✔️ Creating the required working directory.
* ✔️ Identifying the logged-in user.
* ✔️ Recording user group information.
* ✔️ Verifying the active shell.
* ✔️ Recording the current working directory.
* ✔️ Listing directory contents.
* ✔️ Confirming internet connectivity.
* ✔️ Generating and validating the `Environment_Report.txt` file.

---

**Status:** ✅ **Question 1 Completed Successfully**
