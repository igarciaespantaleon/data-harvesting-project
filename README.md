# data-harvesting-project

The **Residential School System** in Canada was a network of government-funded, church-run boarding schools that operated from the late 19th century to 1996. Its goal was to forcibly assimilate Indigenous children into Euro-Canadian culture. Thousands of them died due to harsh conditions, disease, and mistreatment.

The **Truth and Reconciliation Commission (TRC)** documented the trauma and legacy of residential schools. This project automates the process of extracting location-based data from the interactive ArcGIS map that the Comission uses in its memorial website and aims to enhance visualizations and conduct analysis based on the recovered data.

## Project Overview

Web Automation & Data Retrieval:

Automate the navigation of an ArcGIS web application.
Enable specific layers and interact with map elements.
Extract geographic data from the displayed popups.
Error Handling & Adaptive Scraping.

Data Storage & Export:

Storing the extracted data (location names, latitude, longitude) and saving the cleaned dataset in CSV format for analysis and visualization.

Data visualization and analysis:

The second part of the project consists of the analysis of the scraped data through visualization. This includes a thorough cleaning and processing of the generated data tables. The plots and maps are displayed on a shiny app that allows interactivity.


Required Packages:


library(RSelenium)    # Web automation and dynamic web scraping

library(tidyverse)    # Data manipulation, cleaning, and transformation

library(rvest)        # Static web scraping (if needed)

library(writexl)      # Exporting processed data to Excel/CSV

Authors:

Rocío Galeote Ramírez and Irene García-Espantaleón Artal.


# Installation and Setup

## 1. Install Software

Ensure you have the following installed:

R (Programming Language)
Java (Required for Selenium)
Docker (For the Selenium container)
VNC Viewer (Optional, for visual debugging)

## 2. Set Up Selenium
Before running the script, start a Selenium container in Docker:

docker run -d -p 4449:4444 -p 5901:5900 --platform linux/amd64 selenium/standalone-firefox-debug:latest

## 3. Run the Script
Once all dependencies are installed, execute the scraping script in R

