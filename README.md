FileNameTagging
===============


## Proposed Convention for File Naming with Tags
### File Name Tagging

>"It belongs to the wise man to order things."

I have considered long (several months) and hard (for me) how to organize my files. Here I want to propose a "standard" for filenames that would allow sorting files by tags or labels. 

I propose ending filenames with the tags. The filenames are then sorted on the tags, not the filename. The standard can be used for bookmarks, posts, or filenames, or anything that needs to be organized.

#### Level 1:

This is the simplest level. Like so:

`My filename writing.txt`

I can't recommend this because it would lead to confusion about which files were tagged and which were untagged.

#### Level 2:

The next level is to append a special character like "-" next to the tags. I call that character "the tag flag character." Like so:

`My filename writing-.txt`

This gives us at least one tag to sort by. By using a special tag flag character the program can determine if there are tags in the filename or if the file is untagged. Untagged files would be in a separate sort by plain alphabetical.

*OPTION: Level 2 can be modified* and the tag flag can be put at the beginning of the tag. It is a programmer's preference. Example:

`my filename -writing.txt`

The reasoning for the location of the tag flag character is discussed elsewhere in the simple sort workflow:

https://github.com/Kellytom/FileNameTagging/blob/master/Simple%20Sorter%20Workflow%20with%20a%20Spreadsheet.md

I prefer this solution:

`my filename -writing.txt`

putting the flag character at the beginning of the tag, along with a space.

#### Level 3:

The next level is to put as many tags as desired, including numbers or letters for sequential order. For example:

`filename1 -002 -writing.txt`
`filename2 -003 -writing.txt`
`filename3 -001 -writing.txt`
`filename4 -qqq -writing.txt`
`filename5 -qqr -writing.txt`

#### Level 4:

*Programs and apps:*

The rest of the proposed convention would have to do with programs and methods to do the sorting and tagging of different files or bookmarks or posts. 

- The advantage of this system is that it can be used immediately with most existing programs that do file searches. For example, a sort for "-fun" would turn up all files including the word "-fun". The disadvantage is that if the filename includes the word fun, and it is delimited by "-" ahead of time, a search would find "-fun" in a file that was untagged. I hope this is a minor fact. For example:

`Girls-just-want-to-have-fun.txt` would be found in a search. A dedicated spreadsheet or program would detect the " -" space before the dash.



- Each operating system and program would need a separate method to view, sort, and rename the files.

- I would call the program that uses this convention just to view and sort the files and perhaps rename them a "helping program."

- I have done a simple proof of concept in a spreadsheet. This involves no programming, no if statements and no loops. Check it out at:

https://github.com/Kellytom/FileNameTagging/blob/master/Simple%20Sorter%20Workflow%20with%20a%20Spreadsheet.md

- Perhaps the absolute simplest solution for a programmer would be that the filenames could be sorted by direct reverse order. Direct reverse order would give a sort result something like:

`(1gat- 1enamelif):`  
`filename1 -tag1.txt`    
``  
`(1gat- 2gat- 3enamelif):`  
`filename3 -tag1 -tag2.txt`  
``  
`(1gat- 3gat- 2enamelif):`  
`filename2 -tag1 -tag3.txt`

This would basically sort on the last tag, then the second to- last tag, etc.

- The next step is to parse or sort in a more complicated way. Each tag could make a separate entry for the file, e.g.

`filename tag1- tag2-.txt`

results in:

`tag1- filename1.txt  
tag2- filename1.txt`

At minimum, the helping program would give a view of the files sorted by tag. Then the files could be opened in their respective applications by hand. 

A more robust solution would allow the user to add tags, rename files, and open them on a click. An ordered list of files could be changes to insert, remove, or reorder the files. For example, if files were numbered 1 to 100, and a new file added at 57, everything after 57 would automatically be renumberd to 101. 

A list of links could be exported in various file formats, including HTML to make a webpage.

#### Level 5:

*The checking and safety features would include:* 

- to make sure the filenames are not too long,
- make sure the user does not enter unsafe characters.
- make sure the rename does not conflict with an open file.
- make sure the user doesn't enter the dash himself, resulting in a double dash.


#### Level 6:

I am dreaming, but I would like to see all major vendors adopt this standard and incorporate it into their finders and browsers and file operating systems. Then I would not have to program anything, and I could import my text files into an editor in the correct order. I could select just the files I wanted to write a paper or a book. It would be fun.

#### Variations

- Use another character at the end, instead of "-"; "the tag flag character" I could recommend any one of these: "-,Q,QQ, _,=,>" Personally I like "-"

- Put the "tag flag character" before and after every tag, for example:

`filename -write- -edit- -scrivener-.txt`

A programmer might have good reasons for this.

#### Principles

- KISS - Keep it simple. 
- Make the smallest possible change.
- Make the change as  universal as possible.

#### Background

As I said before, I have considered long  and hard how to organize my files. These are the methods and programs I have tried or partially investigated:

- Scrivener
- Markdown
- Wordpresss
- Evernote
- Dropbox
- Google Drive
- Sublime Text 2
- etc.

I want to write articles, small books, programs, scripts and posts. I need to organize the material (clips, snippets, scraps) into drafts. The drafts need to be reorganized into finished works. Each step requires easy reorganization. That is why I want to use this file naming scheme.

The operating systems and programs involved include Windows, ios, Dropbox, Google Drive, Evernote, and others. The other operating systems this standard should be compatible with are ones I don't use: Linux, any *nix, OS X, etc. but I am ignorant of their details. I need to do some research here.

#### The Simplest method

The simplest method would be to take the clipboard, sort it, and put it back on the clipboard. The sort would be a simple reverse order sort so the file would look like this:

`1gat- enamelif` 

The clipboard might look like this:

`(1gat- 1enamelif):`  
`filename1 -tag1.txt`    
``  
`(1gat- 2gat- 3enamelif):`  
`filename3 -tag1 -tag2.txt`  
``  
`(1gat- 3gat- 2enamelif):`  
`filename2 -tag1 -tag3.txt`

#### What is in this Git collection:

https://github.com/Kellytom/FileNameTagging/blob/master/Comments.md

- my comments, and please feel free to add your own.

https://github.com/Kellytom/FileNameTagging/blob/master/To%20Do.md

- my to do list, and please feel free to add your own.
 
https://github.com/Kellytom/FileNameTagging/blob/master/Wishlist.md

- my wishlist, and please feel free to add your own.

https://github.com/Kellytom/FileNameTagging/blob/master/Roadmap.md

- my roadmap, and please feel free to add your own.

https://github.com/Kellytom/FileNameTagging/blob/master/Outline%20of%20Simple%20Sorter%20Program.md

- my pseudo code, and please feel free to add your own.

https://github.com/Kellytom/FileNameTagging/blob/master/Simple%20Sorter%20Workflow%20with%20a%20Spreadsheet.md

- my Workflows, and please feel free to add your own.


#### Conclusion

Input and suggestions are welcome. I am just an amateur hacker, so any robust programming will have to be done by someone else. I will pursue some simple ideas in python, pythonista, and perhaps visual basic.
