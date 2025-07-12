# 🔬 Scholar Research Assistant

An advanced desktop application built with Python to automate scraping, formatting, and randomizing academic references from Google Scholar, streamlining the literature review process.

---

## Table of Contents

- [About The Project](#about-the-project)
- [Key Features](#key-features)
- [Getting Started](#getting-started)
  - [Prerequisites](#prerequisites)
  - [Installation](#installation)
- [How It Works](#how-it-works)
- [Built With](#built-with)

---

## About The Project

As researchers, we often spend hours manually searching for papers, clicking through pages, and formatting citations. This project was born out of a need to automate that entire workflow. It goes beyond simple scraping by allowing users to build a large "pool" of references across multiple years and pages, and then intelligently sample from that pool to create a unique and unbiased reference list.

The final output is a shuffled, perfectly formatted list of citations ready for download as a `.docx` or `.csv` file, saving valuable time and effort in the research process.

## Key Features

* **✅ Interactive UI:** A user-friendly interface built with Streamlit that guides you through the process.
* **⚙️ Advanced Scraping Strategy:** Define a search topic, select multiple years (2020+), and specify the number of pages to scrape for each year.
* **🤖 Human-in-the-Loop:** The app launches a visible browser, allowing you to solve any CAPTCHAs from Google before the main automated scrape begins, ensuring high success rates.
* **📚 Reference Pool Creation:** Automatically scrapes paper titles, authors, and years to build a large, local pool of potential references.
* **🎲 Intelligent Reference Mixing:**
    * Randomly sample a specific number of references from the entire pool.
    * Use "Stratified Sampling" to choose a specific number of random papers from each year.
* **🔀 Final Review & Shuffling:** The final generated list is shuffled to ensure randomness and is presented for a final review before citation scraping.
* **📄 Multiple Export Formats:** Download your final reference list as a numbered list in a **Word (.docx)** file or as a simple **CSV** file.

## Getting Started

The application is distributed as a self-installing executable for Windows, making setup quick and easy.

### Prerequisites

Before you begin, ensure you have the following on your system:

* **Python:** The application requires a modern version of Python. You can get it from [python.org](https://www.python.org/).
    * **Important:** During installation, make sure to check the box that says **"Add Python to PATH"**.
* **Google Chrome:** The automation is built to use the Chrome browser.

### Installation

1.  Download the `ScholarScraper_Setup.exe` file from the repository's releases.
2.  Double-click the setup file to run it.
3.  A terminal window will open and automatically perform a one-time setup:
    * It creates a safe, local virtual environment for the app.
    * It installs all necessary Python packages (`streamlit`, `selenium`, etc.). This may take a few minutes.
4.  Once the setup is complete, the application will launch automatically in your default web browser.

Future launches will be much faster as the setup step is skipped.

## How It Works

1.  **Set Strategy:** Use the sidebar to enter your topic, select the year(s) to search, and choose how many pages to scrape.
2.  **Launch & Prepare:** The app opens a Chrome window. Solve any CAPTCHA that appears.
3.  **Scrape:** Return to the app and click "Scrape All Pages." The tool will take over and build the reference pool in the background.
4.  **Mix & Generate:** Use the "Build Your Reference List" UI to create your final, randomized list from the pool using the "Any" or "Choose" strategy.
5.  **Review & Get Citations:** Give your list a final check, unchecking any papers you wish to exclude. Click the button to get the formatted citations.
6.  **Download:** The final, formatted references appear. Use the buttons to download your list as a `.docx` or `.csv` file.

## Built With

This project was made possible by these incredible open-source libraries:

* [Streamlit](https://streamlit.io/)
* [Selenium](https://www.selenium.dev/)
* [Pandas](https://pandas.pydata.org/)
* [python-docx](https://python-docx.readthedocs.io/en/latest/)
* [PyInstaller](https://pyinstaller.org/en/stable/)
* [Inno Setup](https://jrsoftware.org/isinfo.php)
