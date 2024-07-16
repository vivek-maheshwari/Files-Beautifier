# File Beautifier

This script automates the beautification of files (HTML, CSS, JavaScript, and PHP) within a specified directory. It utilizes various beautification libraries to enhance readability and consistency of code.

## Features

- Automatically beautifies HTML, CSS, JavaScript, and PHP files in a directory.
- Counts and displays the number of files beautified for each file type.

## Usage

### Prerequisites

- Python 3.x installed on your system.
- Required libraries (`jsbeautifier`, `autopep8`, `beautifulsoup4`, `cssbeautifier`) installed. You can install these using pip:

  ```bash
  pip install jsbeautifier autopep8 beautifulsoup4 cssbeautifier
  ```

### Setup

1. Clone the repository or download the script (`beautify_files.py`) to your local machine.

2. Open a terminal or command prompt.

3. Navigate to the directory containing `beautify_files.py`.

### Execution

Replace `your_directory_path` in the script with the actual path to the directory containing files you want to beautify.

```bash
python beautify_files.py
```

### Output

After execution, the script will display the number of files beautified for each file type (`html`, `css`, `js`, `php`).

## Notes

- Ensure you have appropriate permissions to modify files within the specified directory.
- Back up your files before running the script, especially if working with critical codebases.

Feel free to customize the script according to your needs and preferences. If you encounter any issues or have suggestions for improvement, please feel free to create an issue or contribute to the development
