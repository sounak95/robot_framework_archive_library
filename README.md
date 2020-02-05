# robot_framework_archive_library
ArchiveLibrary is a robot framework library to handle ZIP and possibly other archive formats.

ArchiveLibrary
Library scope:	global
Named arguments:	supported
Introduction
ArchiveLibrary is a robot framework keyword library to handle ZIP and possibly other archive formats.

Shortcuts
Archive Should Contain File · Create Compressed File From Files In Directory · Extract File
Keywords
Keyword	Arguments	Documentation
Archive Should Contain File	zfile, filename	
Check if a file exists in the ZIP file without extracting it

zfile the path to the ZIP file

filename name of the file to search for in zfile

Create Compressed File From Files In Directory	directory, compressed_file_path, sub_directories=False	
|Usage| Take all files specified in the 'directory' and create a compressed package from them and store it in the specified 'compressed_file_path'.

|Arguments| directory: Path to the directory that holds our files. compressed_file_path: Path to store our destination package (zip, tar, war, jar, ear). sub_directories: Shall files in sub-directories be included - False by default.

|Example| * Variables * ${directory} D:/extractedjardata * Test Cases * Create Compressed File From Files In Directory ${directory} C:/BOHistoryDetails.jar

Extract File	compressed_file_path, destination=None	
|Usage| Extract the contents of the compressed 'file' into a 'dest' path.

|Arguments| file: Path to the package (zip, tar, war, jar, ear). dest: Destination path to extract the package. By default takes current directory.

|Example| * Variables * ${destination} D:/extracted_data * Test Cases * Extract File C:/Uxp.war ${destination}

Altogether 3 keywords. 
Generated by Libdoc on 2020-02-05 16:31:59.

