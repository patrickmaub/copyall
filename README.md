
# CopyAll: Extract and Copy Directory Contents to Clipboard

`CopyAll` is a Python script designed to extract content from various file types within a directory and copy the aggregated content to your clipboard. It's especially useful for submitting code or text files to Large Language Models (LLMs) like [Claude.ai](https://claude.ai) for analysis or processing.

## Features

- **Supports Multiple File Types**: Works with a wide range of text-based files, including code files, Markdown, plain text, and even documents like `.docx` and `.pdf`.
- **Customizable Extensions**: Specify which file extensions to include or use the default set.
- **Clipboard Management**: Optionally save your current clipboard content before overwriting and restore it later.
- **Verbose Output**: Get detailed information about the script's operation for debugging or logging purposes.

## Table of Contents

- [Installation](#installation)
- [Usage](#usage)
  - [Basic Usage](#basic-usage)
  - [Options](#options)
- [Examples](#examples)
- [Dependencies](#dependencies)
- [Contributing](#contributing)
- [License](#license)

## Installation

1. **Clone the Repository**

   ```bash
   git clone https://github.com/yourusername/copyall.git
   cd copyall
   ```

2. **Install Required Dependencies**

   Make sure you have Python 3 installed. Then install the necessary Python packages:

   ```bash
   pip install -r requirements.txt
   ```

   Alternatively, install packages individually:

   ```bash
   pip install pyperclip PyPDF2 python-docx
   ```

3. **Make the Script Executable and Accessible as `copyall`**

   To run the script as a command-line tool, modify its permissions and move it to a directory in your system's `PATH`:

   ```bash
   chmod +x copyall
   sudo mv copyall /usr/local/bin/copyall
   ```

   This setup allows you to run the script from anywhere by simply typing `copyall`.

## Usage

### Basic Usage

Run the script with the default settings:

```bash
copyall
```

This will process all supported files in the current directory and copy their content to the clipboard.

### Options

- `directory`: Specify the directory to process. Defaults to the current directory.

  ```bash
  copyall /path/to/directory
  ```

- `-e`, `--extensions`: Comma-separated list of file extensions to include.

  ```bash
  copyall -e py,md,txt
  ```

- `-v`, `--verbose`: Enable verbose output.

  ```bash
  copyall -v
  ```

- `-s`, `--save`: Save the current clipboard content before copying new content.

  ```bash
  copyall -s
  ```

- `-r`, `--restore`: Restore previously saved clipboard content.

  ```bash
  copyall -r
  ```

## Examples

1. **Process a Specific Directory with Default Extensions**

   ```bash
   copyall /path/to/directory
   ```

2. **Process Current Directory with Specific Extensions**

   ```bash
   copyall -e py,js,html
   ```

3. **Save Current Clipboard Content and Enable Verbose Output**

   ```bash
   copyall -s -v
   ```

4. **Restore Previously Saved Clipboard Content**

   ```bash
   copyall -r
   ```

## Dependencies

- **Python 3**: Ensure you have Python 3 installed.
- **Required Python Packages**:
  - `pyperclip`: For clipboard operations.
  - `PyPDF2`: To extract text from PDF files.
  - `python-docx`: To extract text from `.docx` files.

Install dependencies via `pip`:

```bash
pip install pyperclip PyPDF2 python-docx
```

## Contributing

Contributions are welcome! Please fork the repository and submit a pull request.

1. Fork it
2. Create your feature branch (`git checkout -b feature/awesome-feature`)
3. Commit your changes (`git commit -am 'Add awesome feature'`)
4. Push to the branch (`git push origin feature/awesome-feature`)
5. Create a new Pull Request
