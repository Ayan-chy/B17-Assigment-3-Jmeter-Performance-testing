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

## Screenshots of Request Summary & Statistics (Booking Load Testing)
<img width="721" height="421" alt="image" src="https://github.com/user-attachments/assets/f95690dc-ded4-47af-8285-44888a5e7afb" />
<img width="1479" height="515" alt="image" src="https://github.com/user-attachments/assets/75c1a06a-9c1c-4a0a-af57-ace08876be5b" />

## Screenshot of Steps (Booking Load Testing)
<img width="894" height="279" alt="image" src="https://github.com/user-attachments/assets/ee4d52e6-3751-49a0-85fd-4488473e07d8" />

## Screenshots of Request Summary & Statistics (Booking Stress Testing)
-35,000 Users/10 Min
<img width="831" height="424" alt="image" src="https://github.com/user-attachments/assets/638eaa41-a1d4-4668-9cd2-a64e1fd0a787" />
<img width="1358" height="499" alt="image" src="https://github.com/user-attachments/assets/251971be-6b49-4105-95b0-a49e22afe987" />
-45,000 Users/10 Min
<img width="726" height="430" alt="image" src="https://github.com/user-attachments/assets/6a3c4cd1-5883-424f-85d6-65d28016c39b" />
<img width="1485" height="549" alt="image" src="https://github.com/user-attachments/assets/7cbc19e7-8f0d-4f6f-9416-ce7feb21394c" />

## Screenshot of Steps (Booking Stress Testing)
<img width="891" height="403" alt="image" src="https://github.com/user-attachments/assets/93c53d14-b507-480c-bd66-ddb51329a5c2" />


## Screenshots of Request Summary & Statistics (Dmoney API Chaining)
<img width="724" height="435" alt="image" src="https://github.com/user-attachments/assets/d6997d97-940b-4b25-87ed-53a3b2020dd5" />
<img width="1471" height="644" alt="image" src="https://github.com/user-attachments/assets/7291b42e-9dff-4886-8e26-da0793bb497b" />










