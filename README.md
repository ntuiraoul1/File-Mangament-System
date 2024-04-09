# File-Mangament-System
Libraries: We import dart:io for file system interactions.
Action enum: We define an Action enum to represent supported actions (list, delete).
Main Function:
It checks if enough arguments are provided (action and filename).
It parses the action string and converts it to an Action enum value using a try...catch block to handle invalid actions.
It extracts the file path from the arguments.
Based on the action, it calls the appropriate function: _listDirectory or _deleteFile.
_listDirectory function:
 Takes a directory path as input.
 Checks if the directory exists using existsSync.
 If the directory is empty, it prints a message.
 Otherwise, it lists all files in the directory using listSync.
 _deleteFile function:
 Takes a file path as input.
 Checks if the file exists using existsSync.
 If the file exists, it attempts to delete it using deleteSync within a try...catch block.
 In case of a FileSystemException, it prints an error message.

Note:
 This is a basic example. You can extend it to support more actions (create directory, move/rename files, etc.).
 For production use, consider adding features like confirmation prompts before deletion and error handling for non-existent directories.
 This program currently only works with files, not directories.
