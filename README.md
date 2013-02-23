FileNameTagging
===============


## Proposed Convention for File Naming with Tags
### File Name Tagging

I have considered long (several months) and hard (for me) how to organize my files. Here I want to propose a "standard" for filenames that would allow sorting files by tags or labels. The operating systems and programs involved include Windows, ios Dropbox, Google Drive, Evernote, and others. The other operating systems are ones I don't use: Linux, any ix, OS X, etc. so I am ignorant of their details.

I propose ending filenames with the tags. The filenames are then sorted in reverse order. The standard can be used for bookmarks, posts, or filenames, or anything that needs to be organized.

#### Level 1:

This is the simplest level. Like so:

`My filename writing.txt`

#### Level 2:

The next level is to append a special character like "-" at the end of the filename. I call that character "the tag flag character." Like so:

`My filename writing-.txt`

This gives us at least one tag to sort by.

*Level 2 can be skipped* and the tag flag can be put at the beginning of the tag. It is a programmer's preference. Example:

`my filename -writing.txt`



#### Level 3:

The next level is to put as many tags as possible, including numbers or letters for sequential order. For example:

`filename1 -002 -writing.txt`
`filename2 -003 -writing.txt`
`filename3 -001 -writing.txt`
`filename4 -qqq -writing.txt`
`filename5 -qqr -writing.txt`

#### Level 4:

*Programs and apps:*

The rest of the proposed convention would have to do with programs and methods to do the sorting and tagging of different files or bookmarks or posts. 

- The advantage of this system is that it can be used immediately with most existing programs that do file searches. For example, a sort for "-fun" would turn up all files including the word "-fun". The disadvantage is that if the filename includes the word fun, and it is delimited by "-" ahead of time, a search would find "-fun" in a file that was untagged. I hope this is a minor fact. For example:

`Girls-just-want-to-have-fun.txt` would be found in a search.


- Each system and program would need a separate method to view, sort, and rename the files.

- I would call the program that uses this convention just to view and sort the files and perhaps rename them a "helping program."

- The absolute simplest solution would be that the filenames could be sorted by direct reverse order Direct reverse order would give a sort result something like:

`(1gat- enamelif.txt):`  
`filename tag1-.txt`    
`(1gat- -2gat enamelif.txt):`  
`filename tag1- tag2-.txt`  
`(-1gat- -3gat enamelif.txt):`  
`filename tag1- tag3-.txt`

This would basically sort on the last tag, then the second to- last tag, etc.

- The next step is to parse or sort in a more complicated way. Each tag could make a separate entry for the file, e.g.

`filename tag1- tag2-.txt`

results in:

`tag1- filename.txt  
tag2- filename.txt`

At minimum, the helping program would give a view of the files sorted by tag. Then the files could be opened in their respective applications by hand.

#### Level 5:

*The checking and safety features would include:* 

- to make sure the filenames are not too long,
- make sure the user does not enter unsafe characters.
- make sure the rename does not conflict with an open file.

#### Variations

- Use another character at the end, instead of "-"; "the tag flag character" I could recommend any one of these: "-,Q,QQ, _" Personally I like "-"

- Put the "tag flag character" after every tag, for example:

`filename write- edit- scrivener-.txt`


#### Principles

- KISS - Keep it simple. 
- Make the smallest possible change.
- Make the change as  universal as possible.

#### Background

As I said before, I have considered long  and hard how to organize my files. More on that here. These are the methods and programs I have tried or investigated:

- Scrivener
- Markdown
- Wordpresss
- Evernote
- etc.

I want to write articles, small books, programs, scripts and posts. I need to organize the material (clips, snippets, scraps) into drafts. The drafts need to be reorganized into finished works. Each step requires easy reorganization. That is why I want to use this file naming scheme.

#### The Simplest method

The simplest method would be to take the clipboard, sort it, and put it back on the clipboard. The sort would be a simple reverse order sort so the file would look like this:

`-1gat enamelif.txt` 

The clipboard might look like this:

`(-1gat enamelif.txt):`  
`filename tag1-.txt`    
`(-1gat -2gat enamelif.txt):`  
`filename tag1- tag2-.txt`  
`(-1gat -3gat enamelif.txt):`  
`filename tag1- tag3-.txt`

#### What is in this Git collection:

https://github.com/Kellytom/FileNameTagging/blob/master/Comments.md
https://github.com/Kellytom/FileNameTagging/blob/master/To%20Do.md
https://github.com/Kellytom/FileNameTagging/blob/master/Wishlist.md
https://github.com/Kellytom/FileNameTagging/blob/master/Roadmap.md
https://github.com/Kellytom/FileNameTagging/blob/master/Outline%20of%20Simple%20Sorter%20Program.md
https://github.com/Kellytom/FileNameTagging/blob/master/Simple%20Sorter%20Workflow%20with%20a%20Spreadsheet.md
#### Conclusion

Input and suggestions are welcome. I am just an amateur hacker, so any robust programming will have to be done by someone else. I will pursue some simple ideas in python, pythonista, and perhaps visual basic.
