# Project Title:Jmeter Performance Testing

## Overview
This repository contains JMeter test plans, test data, and generated HTML reports for the assignments on load test & API Chaining using Jmeter .

## Repository Structure
- `Dmoney.jtl` — sample results file at repo root
- `Dmoney/` — JMeter test plan and resources for the Dmoney scenario
  - `Dmoney.jmx` — JMeter test plan
  - `Resources/` — CSV data files (`Deposit.csv`, `Payment.csv`, `SendMoney.csv`)
- `Booking/` — JMeter test plan for booking scenario
  - `booking.jmx`
- `Reports/` — generated HTML reports and statistics JSON
  - `index.html` — dashboard entry
  - `statistics.json`
  - `content/` — CSS/JS assets used by the dashboard

## Prerequisites
- Java 8+ installed and on `PATH`
- Apache JMeter 5.x installed
- A modern browser to open the HTML report

## How to Run (examples)
Run a JMeter test non-GUI and generate an HTML report:

Dmoney API Chaining example (PowerShell/CMD):

jmeter -n -t Dmoney/Dmoney.jmx -l Dmoney/Dmoney.jtl -j jmeter_dmoney.log -e -o Reports/dmoney_report

Load test- Booking example:

jmeter -n -t Booking/booking.jmx -l Booking/booking.jtl -j jmeter_booking.log -e -o Reports/booking_report

Notes:
- The `-n` flag runs JMeter in non-GUI mode.
- The `-e -o <folder>` options generate an HTML report in the specified folder.
- Ensure the output report folder does not already exist or is empty.

## Test Data
Test CSVs are in `Dmoney/Resources/` and are referenced by the respective JMX files.



