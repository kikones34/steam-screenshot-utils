# SSU: Steam Screenshot Utils

Utilities for sorting, backing up and merging steam screenshots.

- Back up Steam screenshots by specifying your Steam user folder.

  Categorizes them into folders with the corresponding app names.
  
  (Useful when you don't have the "Save uncompressed copy" option enabled).

- Sort uncompressed screenshots into folders with the corresponding app names.

  (Useful when you have the "Save uncompressed copy" option enabled).

- Merge backed up compressed screenshots with sorted uncompressed screenshots.

  This copies compressed screenshots to the uncompressed screenshots folder whenever
  an uncompressed copy of them is not found.
  
  (The compressed screenshots backup can be safely removed after this).
  
  (Useful when you didn't have "Save uncompressed copy" activated at the beginning,
  but activated it at some point afterwards).

# Usage

```
ssu backup <steam_user_folder> [-o <output_folder>]
ssu sort <screenshots_folder>
ssu merge <compressed_screenshots> <uncompressed_screenshots>
```

Notes:

- Your steam user folder is in Steam/userdata/<user_id>.
- Sorting doesn't have an output argument becasue it's done in-place.
- For merging, the compressed screenshots folder is expected to be the output of the backup command,
  and the uncompressed screenshots folder is expected to be the output of the sort command.
      
# Requirements

This script requires Python 3.6 or newer. Install the required packages by executing:

```
pip install -r requirements.txt
````
