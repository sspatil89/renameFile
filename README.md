# renameFile
"""
Renames the multiple file type filenames within the same directory with appending number
Usage:
python renameFile.py
"""

import os

path = 'Enter the file path'
files = os.listdir(path)
i = 1

for file in files:
    filename, file_extension = os.path.splitext(file)
    os.rename(os.path.join(path, file), os.path.join(path, filename + str(i) + file_extension))
    i = i+1
