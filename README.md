# Unzip files from Google Drive with Python

This repository contains a script that allows you to connect to your Google Drive, read a zip file and unzip it. The unzipped file will be directly stored in your Google Drive, this is very useful because there is no option to unzip a file directly from the Google Drive UI.

## How it works
There is one script called `main.ipynb` and here is a description of what it does.

First, we import `shutil`. This library will be used to unzip the zip file.

```python
import shutil
```

After that, we connect to our Google Drive.

```python
from google.colab import drive

drive.mount('/content/drive')
```

Finally, we specify the location of the zip file. Make sure to change `path_to_file_dir` and `your_file.zip`

```python
file_dir_path = "/path_to_file_dir"

shutil.unpack_archive(f"{file_dir_path}/your_file.zip", file_dir_path)
```

I hope this helps.
