# Api Documentation

## Mangas
` GET /mangas `
* No Data required
* returns List with following content
```
manganame
url_friendly_name
```
---
` GET /manga/"url_friendly_name" `
* Optional session cookie
* returns List with following content
```
Description
Chapters
  - Chapter Names
  - Volume
  - Chapter Number
if user token was specified hidden mangas can be seen too
```
---
` GET /manga/"url_friendly_name/dl" `
* session cookie
* returns a zip
```
zip 
```
---
` POST /manga/new `
* session cookie
* Manga Object
```
Description
Thumbnail
Name
Author
Artist
reading style
```
---
` PUT /manga/"url_friendly_name" `
* session cookie
* Manga Object
```
Description
Thumbnail
Name
Author
Artist
reading style
```
---
### Chapters
` GET /manga/"url_friendly_name"/"chapter_number"`
* session cookie
* returns following stuff
```
Total Page Count
List
  Pagenumber
  URL
if session cookie was supplied hidden chapters can be show too
```
---
` POST /manga/"url_friendly_name"/new`
* session cookie
* Chapter Object
```
Chapter Name
Chapter Volume
Chapter Number
Chapter File (zip)
Release Date (optional default is now())
Hidden (optional default is visible)
```
---
` PUT /manga/"url_friendly_name"/"chapter_number"`
* session cookie
* Chapter Object
```
Chapter Name
Chapter Volume
Chapter Number
Chapter File (zip)
Release Date (optional default is now())
Hidden (optional default is visible)
```
---

