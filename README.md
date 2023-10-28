# FTP Manager Python Package

The **FTP Manager** Python package provides a convenient and easy-to-use interface for managing files on FTP servers. It simplifies tasks such as listing folders, uploading files, downloading files, and creating new folders on the FTP server. Whether you're dealing with large datasets or just a few files, this package makes FTP file management straightforward and efficient.

## Installation

You can install the **FTP Manager** package via pip:

```bash
pip install FTP_manager

Usage

Here's how you can use the FTP Manager package in your Python projects:

from FTP_manager import FTPManager

# Initialize FTPManager with host, username, and password
host = 'ftp.example.com'
username = 'your_username'
password = 'your_password'
ftp_manager = FTPManager(host, username, password)

# List top-level folders on the FTP server
top_level_folders = ftp_manager.list_top_level_folders()
print("Top Level Folders:", top_level_folders)

# Upload a DataFrame as a CSV file to a remote folder
import pandas as pd
data = {'Column1': [1, 2, 3], 'Column2': ['A', 'B', 'C']}
df = pd.DataFrame(data)
remote_folder = 'data'
file_name = 'data_file'
ftp_manager.upload_file(df, remote_folder, file_name)

# Download a CSV file from the FTP server as a DataFrame
downloaded_data = ftp_manager.download_file(remote_folder, file_name)
print("Downloaded Data:")
print(downloaded_data)

# Create a new folder on the FTP server
new_folder_name = 'new_folder'
ftp_manager.create_folder(new_folder_name)

