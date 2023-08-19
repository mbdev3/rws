# RWS (Remove White Spaces)

The `rws` (Remove White Spaces) script is a utility that removes extra white spaces from `className` attributes in JSX and other supported file types. It recursively traverses through directories, processes files, and updates class names to remove extra white spaces while maintaining a single space between class names.

## Installation

To use the `rws` script, follow these steps:

1. Create a file named `rws.js` in your project's root directory.

2. Copy and paste the contents of the `rws.js` script into the newly created file.

## Usage

1. Open a terminal and navigate to your project's root directory.

2. Run the `rws` script using the following command:

   ```bash
   node rws.js [rootDirectory]
   ```

   Replace `[rootDirectory]` with the path to the directory you want to process. If no directory is provided, the script will default to using `./`.

   Example 1: Process files in the current directory (`./`):

   ```bash
   node rws.js
   ```

   Example 2: Process files in a specific directory:

   ```bash
   node rws.js /path/to/your/root/directory
   ```

   This will execute the script, which will recursively traverse through directories, process supported files, and remove extra white spaces from `className` attributes.

## Configuration

The script allows you to configure certain directories that should be ignored during processing. To customize this setting, open the `rws.js` file and locate the `directoriesToIgnore` array at the top of the script. You can add directory names to this array that you want the script to skip processing.

```javascript
const directoriesToIgnore = ["node_modules", ".git", ".next"]; // Add or remove more directories as needed
```

## Custom File Types

You can also configure the list of accepted file types that the script should process. Open the `rws.js` file and locate the `acceptedFileExtensions` array at the top of the script. Add or remove file extensions as needed.

```javascript
const acceptedFileExtensions = [".js", ".jsx", ".ts", ".tsx"]; // Add or remove more extensions as needed
```

## Notes

- Before using the script, make sure to back up your files or work on a subset of files to ensure the desired outcome.

- This script modifies files directly. Make sure you're using version control (such as Git) to track changes and revert them if necessary.
