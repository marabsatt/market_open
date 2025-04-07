# U.S. Stock Market Open Checker

## Overview

This notebook determines whether the U.S. stock market (NYSE) is currently open. It considers time zones, weekends, and U.S. market holidays using the `holidays` library. If the market is closed, the script will calculate how long until the next market open and pause execution until that time.

## Features

- Automatically detects current time in Eastern Standard Time (EST)
- Checks for U.S. holidays using the `holidays` library
- Determines if the market is open (between 9:30 AM – 4:00 PM EST)
- Sleeps until the next market open when closed
- Recursively ensures it only proceeds during open hours

## Use Cases

- Automating trading scripts that should only run when the market is open
- Integrating with broker APIs that require timing constraints
- Scheduling batch trading operations or scraping routines

## Key Functions

- `market_is_open()`: Checks if the market is currently open. If not, triggers a wait.
- `sleep_till_open()`: Calculates the exact time until the next trading window and puts the script to sleep until then.

## Setup
1. Open `market_open.ipynb`
2. Run all cells sequentially
3. If the market is closed, the notebook will wait until the next open window before proceeding.

## *Disclaimer*

*This utility is intended for educational and development purposes only. Production use should include additional error handling and scheduling controls.*

### Prerequisites

Install the required libraries:

```bash
pip install holidays pytz python-dateutil
