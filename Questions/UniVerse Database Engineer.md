
# UniVerse Database Engineer

## Files and Design

### What are some of the different file types?

| File type | Type 					| Description
|-----------|-----------------------|----------------------------------------------------
| 1 & 19	| directory				|
| 2			| static				| Keys end with numbers.
| 3			| static				| Keys end mainly with numbers.
| 4			| static				| Keys end with letters.
| 5			| static				| Keys end with full range of ASCII characters.
| 6			| static				| Keys begin with numbers.
| 7			| static				| Keys begin mainly with numbers.
| 8			| static				| Keys begin with letters.
| 9			| static				| Keys begin with full range of ASCII characters.
| 10		| static				| Keys are numbers.
| 11		| static				| Keys are mainly numbers.
| 12		| static				| Keys are letters.
| 13		| static				| Keys are full range of ASCII characters.
| 14		| static				| Entire keys are numbers.
| 15		| static				| Entire keys are mainly numbers.
| 16		| static				| Entire keys are letters.
| 17		| static				| Entire keys are full range of ASCII characters.
| 18		| static				| Entire keys are of arbitrary form.
| 30		| dynamic				|

### Why would you use a particular file type over another?

### Explain the terms "modulo" and "separation"

`modulo` is the number of groups the file has. `separation` is the number of 512 bytes disk frames are allocated to each group 

### What are some of the common fields of a dictionary record?

| Field 					| Description
|---------------------------|--------------------------------------------------
| Conversion 				| Blank unless a conversion is required. e.g. D DMY[2,A3,4] would store 1 for 01 JAN 1968
| Column Header 			| Title that appears at the head of the column
| Format 					| The number of characters to display and alignment. 10R - 10 characters, right aligned. 
|							| 10T - 10 characters, text aligned. 10L - 10 characters, left aligned.
| Single or Multi			| S for single value, M for multi-value


## Support

### Describe some of the ways that you'd relieve database processing pressure on poorly performing files?

* resize files

## General

### Describe the difference between named and unnamed common in Universe

### What is a recursive subroutine?
### In what situation might a recursive subroutine be used?
### What special considerations does a programmer need to take in to account when coding a recursive subroutine?

### Describe the concepts behind transaction processing and describe how UniVerse implements transaction processing
### Describe the pessimistic and optimistic approaches to database locking.

### Describe the difference between the SQL NULL and an empty string in Universe.

### Describe the hashed file concept used by the Universe database.
### Describe the type 30 file concept used by the Universe database.
### Other than 1, why should file separations never be an odd number?

So that the boundaries of each file group are more likely to coincide with the boundaries that the host operating system uses to organise its disk which also tends to be a power of two.

### What is the difference between type 1 and type 19 files in Universe?

### What is the difference between a 32 bit and 64 bit file in Universe?

A 32bit file in universe is limited to 2GB in size compared to a 64bit file which can be much larger.

### Why does the UniVerse database support multiple "flavours"?

Primarily to facilitate syntax compatibility for application software written for other types of PICK style databases thus minimising difficulties when migrating or upgrading to a universe database.

### How does the wide zero mechanism work in UniVerse?

When universe compares two numbers for equality, it uses the wide zero configuration parameter to determine how small the difference between the two numbers should be before the difference is considered small enough to be zero versus large enough to be considered non-zero.
