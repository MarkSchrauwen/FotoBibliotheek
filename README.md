# FotoBibliotheek
Goal : Implementation of a Database for a photo library keeping track of file-locations, tags, date, primary theme, etc. Automation of tasks to perform like:
-intake of photos into database;
- renaming photos in a certain format;
- storing files in a structured way (date;primary theme;counter);
- performing queries (date, primary theme, tags,..) etc...

Structure of database: relational database
- Foto_Identificatie: main storage of details about photo (Foto_Id,FotoYear, FotoMonth, FotoDay, Genre_Id, Foto_Teller, FotoExt, FotoPath_Id, FotoDrive_Id, Plaats_Id, FotoTag_Id, Thumbnail)
- Foto_Genre: Genre_Id, Genre
- FotoPath : FotoPath_Id stores the path, driver, server
- FotoPlaats: Plaats_Id, Land, Plaats
- Bridge_FotoTag : bridge between Foto_Id and Tag_Id (many to many relations so that 1 phote can have several tags)
- Foto_Tagging : Tag_Id and Tag
- sqlite_sequence : stores the auto-increment numbers for the fields Foto_Genre, Foto_Tagging, Bridge_FotoTag, Foto_Identificatie
