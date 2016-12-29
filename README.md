# dataextract

Using string manipulation to extract data from raw text.


The set of data I have is a list of random names, addresses and phone numbers. 
This code executes three functions.
First step is opening the text file and setting it’s allias as fo. [with open ('input.txt') as fo:]
Next I need it to read the data line by line before it can extract the data that is ask for. So I’ve told it to navitage tthrough the records of the text file. [for rec in fo:]
And print the records.

with open ('input.txt') as fo:
	for rec in fo:
	    print rec


Lastly it’s using a split function to seperate the data, the value of this delimiter is represented with # in this case. This way it will be possible to extract data as I want.

#To extract the names:

with open ('input.txt') as fo:
	for rec in fo:
	    print rec.split('#')[0]


#To extract the address:

with open ('input.txt') as fo:
	for rec in fo:
	    print rec.split('#')[1]
 
#To extract the phone numbers:

with open ('input.txt') as fo:
	for rec in fo:
	    print rec.split('#')[2]



The delimiters can be used to post multiple segments of data together.
#To extract name and phone number:

with open ('input.txt') as fo:
	for rec in fo:
	    print rec.split('#')[0] + ' --- ' +rec.split('#')[2]
	    
