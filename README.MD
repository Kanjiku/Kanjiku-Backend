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
  - id
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
` DELETE /manga/"url_friendly_name" `
* session cookie
* Manga id or url friendly
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
List of Teams who worked on it
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
### TAGS(Mangas)
` POST /manga/"url_friendly_name"/TAGS`
add tag to manga
* session cookie
* TAG Id
---
` DELETE /manga/"url_friendly_name"/TAGS`
* session cookie
* TAG Id
---
### TAGS
` GET /tags`
* returns list of tags
---
` POST /tags/new`
* session cookie
* Tag Object
```
Tag Name
```
---
` Delete /tags/"TAGNAME"`
* session cookie
---
` GET /tags/"TAGNAME"`
* returns List of Mangas tagged with tags
---
### Config
` GET /config`
* returns page Language
* api version
* default theme
* themes allowed
* num of last chapters
* logo path
* site/group name
---
` POST /config/logo `
*change main logo
---
### Groups
` GET /Team`
*returns list of Team Object
```
ID
Name
Logo
Partner
```
---
` GET /Team/<id>`
*returns list of Team Object
```
List of mangas the group worked on
Description
partner
link

```
` POST /Team/new`
* returns status
* requires Session cookie
* requires Team Object
```
Team Name
Website
Partner Status
Description

```

