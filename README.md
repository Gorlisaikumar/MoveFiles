# MoveFiles
This Python script automates the process of moving all .jpg image files from a source folder to a destination folder on your local machine.  🔧 Features: Scans all files in the source directory.  Moves only .jpg files (case-insensitive).  Prints the name of each file as it's moved.  Confirms successful completion at the end.

#code

import os
import shutil
source_folder = 'source file' 
destination_folder =  'destination file'
if not os.path.exists(destination_folder):
    os.makedirs(destination_folder)
for filename in os.listdir(source_folder):
    if filename.lower().endswith('.jpg'):
        src_path = os.path.join(source_folder, filename)
        dest_path = os.path.join(destination_folder, filename)
        shutil.move(src_path, dest_path)
        print(f"Moved: {filename}")

print("All .jpg files moved successfully.")
