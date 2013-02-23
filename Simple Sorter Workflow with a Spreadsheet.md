##Simple Sorter Workflow with a Spreadsheet

Easier than writing a program or a script would be using a word processor or spreadsheet to sort the file names.

I will try Open Office Calc (Libre Office Calc) because it is free. 

Perhaps the reason sorting by the end of the filename has not been done before is because finding the end of a string and working backwards is not as easy as finding the beginning.

A simple way to sort data is to put it in columns and then sort on a column. The filenames need to be cut up into pieces and then put in separate columns.

Sort on the second to last column in a spreadsheet is not easy to make automatic unless the number of columns is known. For example,

`this is a filename tag1-.txt  
short name tag1-.txt`

In this example, the tags will end up in different columns, unless the "-" is used as a column separator. But if "-" is used as a column separator, then these files will also create problems:

`this-is-a-filename- tag1-.txt  
short-filename.txt`

so the separators are actually two characters, "-." or " -" with the preceding space.

Separating on just the "." gives only 2 columns, so another separator needs to be " -" including the space, for example:

`this-is-a-filename -tag1-.txt`

####First run:
select only the filenames with tags. (search on "-." or ".")

####Second run: 
Divide the tagged filenames into two columns on the " -" characters, and then sort on the second column.

Here is some sample data:

`this-is-a-filename -tag1-.txt  
this is a filename -tag2-.txt   
short name -tag3-.txt`

I ran into problems because I could not see the beginning of the tag unless it was marked. Perhaps there is an easy way around this but for now in a spreadsheet environment I recommend including a dash both before and after the tag like so:
-tag1-. The first dash is preceded by a space, literally " -tag1-".

In a real scripting or coding language, it would be possible to catch errors and also find the space closest to the end of the string. In a simple spreadsheet program, I don't know if it is possible or consistant or wise to search with a REGEX (regular expression) or a loop.

I think it is important to make the tags accessible to spreadsheets and simple coding because the convention should be as easy to reproduce as possible, like markdown and plain text documents.

Here is the sequence of steps in a spreadsheet that allowed me to sort filenames by the tags inside the filenames.

####Method 1:

- copy filename to filetemp.  
- strip out filename from filetemp.  
- Strip out the name so that the tags are all that is left in filetemp.  
- sort each row on the filetemp column.  

- step 1: find the last occurrence of a period “.” in the filename and strip off the extension.
- This sorts by the first tag in the filename, then the second. This behavior might be changed somehow, but I haven't thought it through.
- Once the tags are processed, select all the data and all the columns up to "E". Choose Data/Sort "column E" from the menu. Voila! If I felt like learning enough markdown to make a table I would.

####Here is the original filename data:

short name -tag3-.txt  
short name -tag3- -tag1-.txt  
this is a filename -tag1-.txt  
this is a filename.txt  
This-is-a-filename.txt  
This-is-a-filename -tag2-.txt  
short name.txt  

####Here are the tags in Column E after processing:
`- `  
`-  `  
`-  `  
`-tag1-. -  `  
`-tag2-. -  `  
`-tag3-. -  `  
`-tag3- -tag1-. -  `



####And here are the resulting filenames after sorting:

short name.txt  
this is a filename.txt  
This-is-a-filename.txt  
this is a filename -tag1-.txt  
This-is-a-filename -tag2-.txt  
short name -tag3-.txt  
short name -tag3- -tag1-.txt  

###How to use:

Put the filenames in column "A"
Put the formulae in the correct columns.

####Formulae:

Put this in column "B"  
“=LEFT(A20,FIND(".",A20))”

Put this in column "D"  
“=CONCATENATE(B20," -")”


Put this in column "E"  
“=RIGHT(D20,LEN(D20)-FIND(CONCATENATE(CHAR(32),"-"),D20))”


#### Notes:

An area that could create problems is if a user or program modifies the filenames. That is why a public standard convention could help.

Other possible file tag characters: "> ="


