Script Overview

The script performs the following steps:

Define the target folder
The variable folder_path points to the main directory you want to scan.

folder_path = "yourfolder"


Walk through subdirectories
Using os.walk(), the script iterates through all subfolders and files in the given directory.

Build full file paths
For each file, it constructs the full path and appends it to the file_paths list.

file_path = os.path.join(folder_name, "^", filename)


Print results
Finally, it prints each collected file path.

🧠 Notes

The "^" character in the path join (os.path.join(folder_name, "^", filename)) seems intentional — possibly used as a custom separator for later parsing.
If you intend to get a valid Windows path, replace it with:

file_path = os.path.join(folder_name, filename)


The script uses double backslashes (\\\\) to correctly reference a network path (UNC path).

pandas is commented out; it may be useful later if you plan to export results to a DataFrame or CSV file
