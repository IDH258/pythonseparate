# python separate code

import os
import shutil

source_dir = '\Users\Computer\Desktop\....'

target_dir = '\Users\Computer\Desktop\....'

for root, dirs, files in os.walk(source_dir):
    for file in files:
        if file.endswith(".jpg") or file.endswith(".png"):
            file_path = os.path.join(root, file)
            shutil.move(file_path, target_dir)
