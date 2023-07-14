# SEDAR Scraper

A Python-based web scraper designed to extract data from SEDAR, the Canadian stock exchange filing system. Given that SEDAR uses CAPTCHA for protection, this scraper implements an Optical Character Recognition (OCR) system to bypass this security feature.

## Improvements and Changes

The original script has undergone significant refactoring and improvements, making the code more efficient, readable, and maintainable.

- The code structure has been improved by breaking down tasks into separate functions, each with a specific role.
- The imports have been reorganized to comply with best practices: built-in modules, third-party modules, and application-specific modules.
- A main guard (`if __name__ == "__main__"`) has been added to the script to ensure that the scraping process only occurs when the script is run directly, not when it's imported as a module.
- Docstrings have been added to functions to provide a clear explanation of their functionality, inputs, and outputs. This will help developers in understanding the workflow and also serve as inline documentation.
- The code now uses the modern `f-string` formatting style for print statements, making them more readable and Pythonic.
- `os.makedirs` now uses the `exist_ok=True` argument to eliminate the need for a try/except block. This change makes the creation of new directories more robust and the code more readable.
- `urllib.parse.unquote` is now used instead of `urllib.unquote` to ensure compatibility with Python3.
- The code has been refactored to utilize smaller, more maintainable functions.
- Constant variables are now named in uppercase, as per PEP8 style guidelines, improving code readability.

## Usage

To use this scraper, you simply need to run the script, and it will automatically scrape data from the SEDAR website and store the required information. It includes functions for downloading company documents, extracting company information, and loading all filings. Note that the current code is configured to connect to a local PostgreSQL database; you may need to change the connection string depending on your setup.

## Disclaimer

This tool is meant for educational and research purposes. Please be aware of and respect the terms of service for the website you are scraping.
