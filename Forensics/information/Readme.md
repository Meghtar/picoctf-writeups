# information

Points: 10

## Category

Forensics

## Description
>Files can always be changed in a secret way. Can you find the flag? cat.jpg

## Solution
There is nothing exceptional visually in the photo. However opening file in text editor or using some kind of tool to display metadata will show something like 

```<cc:license rdf:resource='cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9'/>```

There is a text that looks like base64. After decrypting it I got the flag.

Flag:
>picoCTF{the_m3tadata_1s_modified}

