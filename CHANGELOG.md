# CHANGELOG

## [1.0.3] - 2021-03-16

### Important Info
- It was revealed during testing that Sub-Folders are treated as 1 item during the copy counts; Its unlikely that I am going to be able to fix this without a massive refactor. 
This also might cause sub-folder contents to not copy if the destination already contains that sub-folder. Unlikely to fix that issue due to the same refactoring requirements.
Likewise, this script was primarly created to bring template files into new projects/folders. It was never intended for comlex functionality. If you need to combine data structures, I would recomend making a new secondary template for that specific combination of folders/files. 

### Modified
-clone: Had to patch again due to an issue where existing files were getting overwritten. 


## [1.0.2] - 2021-03-16

### Modified
- clone: Added a fix which caused files that started with '.' to be ignored
-- Specifically designed and tested fix to make sure that parent folders are not inadvertantly copied without preventing child folders from copying correctly

## [1.0.1] - 2021-03-15 

### Added
- CHANGELOG.md : This file

### Modified
- clone : Added a fix which cause the script to fail if the source or destination folders included spaces in their names.

## [1.0.0] - 2021-03-14 - Original Upload

### Added
- clone : Contains the actual executable script
- README.md : Contains the documentation for the project
- LICENSE : Contains the legal info for end users


 