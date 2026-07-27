# Configure Folder Permissions Using PowerShell

## Overview
After configuring permissions on individual files, the next step was to configure permissions at the folder level so each security group has the right access to entire shared folders. This also involved moving the `shared-folders` and `csv-files` directories from the Desktop to the `C:\` drive to simplify the file paths used in the script.

## Requirements
A CSV file containing the security groups. It's stored in the repo here:

- [14-CSV-files/OTCS-Security-Groups.csv](../../14-CSV-files/OTCS-Security-Groups.csv)

## Setup

### 1. Create the Script File

