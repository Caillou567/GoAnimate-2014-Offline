Voice Clip Importing Workaround System
for Wrapper: Offline 1.3.0 Beta
version dated February 8, 2022
by KrisAnimate

How this works:
This mod has 3 parts.
- an extra http-server instance to host the voice clip files on an extra localhost port,
- 2 fake text-to-speech voices that connect to the localhost port and blindly take mp3 files with specific names from a
  specific folder, and;
- a modification to the importer batch script - when importing an mp3 file as a voice clip, the importer copies it into the
  folder where either of the fake text-to-speech voices will take it from, and renames the file for either of the the fake
  TTS voices to take (after deleting an existing file with the exact same file name to prevent conflicts)

To install this voice clip workaround:
Extract the contents of this .zip file to a temporary folder.
Copy the folder's contents to the folder where you installed Wrapper Offline 1.3.0 beta, overwriting any existing files.
You might want to make a backup of your existing import.bat, start_wrapper.bat, and the wrapper\tts folder, or your entire
Wrapper: Offline installation first.

To use this voice clip workaround:
Use the new import.bat to import the voice clip you want to import. There are 2 slots available. Select "Any Language" from
the language selector in the text-to-speech dialog box, then select Male for Import Slot 1 or Female for Import Slot 2.
To change the voice clip retrieved by any of the 2 import slots, repeat the entire importing process.

Changes made

February 8, 2022
- Updated to work with latest 1.3.0 beta.
- Reverted to NextUp for Polly voices due to Voicemaker.in backend change. Tried to remove voices Voicemaker has that NextUp
  does not. WARNING: THIS WILL BREAK EXISTING VIDEOS THAT USED THOSE VOICES.
- Added second import slot
May 16, 2021
- Added placeholder voice clip