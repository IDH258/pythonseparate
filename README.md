# pythonseparate

import os
import shutil


# Directory to search for photos
source_dir = '\Users\AMG_Computers\Desktop\fromac\2015\2015.01.14'

# Directory to move photos to
target_dir = '\Users\AMG_Computers\Desktop\fromac\2015'

# Iterate through all subdirectories in source_dir
for root, dirs, files in os.walk(source_dir):
    for file in files:
        # Check if file is a photo
        if file.endswith(".jpg") or file.endswith(".png"):
            # Construct path to file
            file_path = os.path.join(root, file)
            # Move file to target_dir
            shutil.move(file_path, target_dir)
