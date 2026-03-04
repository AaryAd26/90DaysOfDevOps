# Day 17 – Shell Scripting: Loops, Arguments & Error Handling

---

## Task 1: For Loop Practice

### 1. Create `for_loop.sh`

- Write a script that loops through 5 fruit names.
- Print each fruit using a `for` loop.

<img width="591" height="167" alt="Screenshot 2026-03-04 190335" src="https://github.com/user-attachments/assets/6ea62b97-fc56-425e-aa77-d1edb85b9f48" />


---

### 2. Create `count.sh`

- Use a `for` loop to print numbers from 1 to 10.

<img width="553" height="230" alt="Screenshot 2026-03-04 190446" src="https://github.com/user-attachments/assets/136243d6-171f-4455-b2f4-035cea371dd5" />

---

## Task 2: While Loop Practice

### Create `countdown.sh`

- Accept a number from the user.
- Use a `while` loop to count down to 0.
- Print `"Done!"` after the countdown finishes.

<img width="578" height="296" alt="Screenshot 2026-03-04 190533" src="https://github.com/user-attachments/assets/84d499ce-030a-4132-847e-5ef3f6e20dc2" />

---

## Task 3: Command-Line Arguments

### 1. Create `greet.sh`

- Accept a name using `$1`.
- Print: `Hello, <name>!`
- If no argument is passed, display:

  Usage: ./greet.sh <name>
<img width="661" height="77" alt="Screenshot 2026-03-04 190812" src="https://github.com/user-attachments/assets/d6af6790-3d62-4954-b56e-2ca58d8db7fd" />

---

### 2. Create `args_demo.sh`

- Print total number of arguments using `$#`.
- Print all arguments using `$@`.
- Print the script name using `$0`.

<img width="674" height="150" alt="Screenshot 2026-03-04 190818" src="https://github.com/user-attachments/assets/97e1b0df-ae53-453a-bd25-d2e19c938810" />

---

## Task 4: Install Packages Using a Script

### Create `install_packages.sh`

Requirements:

- Define a list of packages: `nginx`, `curl`, `wget`
- Loop through each package.
- Check if the package is installed:
  - Use `dpkg -s` (Debian/Ubuntu)
  - Or `rpm -q` (RHEL/CentOS)
- If not installed → install it.
- If already installed → skip it.
- Print status for each package.

<img width="819" height="217" alt="Screenshot 2026-03-04 190923" src="https://github.com/user-attachments/assets/01788dd8-3917-4469-9ebe-ab4125c6a9c9" />

---

## Task 5: Error Handling in Shell

### 1. Create `safe_script.sh`

- Use `set -e` at the top (exit immediately if any command fails).
- Create directory: `/tmp/devops-test`
- Change into that directory.
- Create a file inside it.
- Use `||` to print an error message if a command fails.

<img width="628" height="58" alt="Screenshot 2026-03-04 191350" src="https://github.com/user-attachments/assets/6657e114-2b2e-4367-a8fb-e70f2c5c902f" />

---

### 2. Modify `install_packages.sh`

- Add a check to ensure the script is run as root.
- If not run as root, exit with a message.

<img width="649" height="67" alt="Screenshot 2026-03-04 191048" src="https://github.com/user-attachments/assets/ce32edde-7103-46d6-89e1-60902f37ecf1" />

---

## What I Learned

- Writing and using `for` loops
- Writing and using `while` loops
- Working with command-line arguments (`$1`, `$#`, `$@`, `$0`)
- Automating package installation
- Handling errors using `set -e` and `||`
- Checking for root privileges in scripts

---
