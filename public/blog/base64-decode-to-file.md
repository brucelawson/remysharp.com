# Base64 decode to file

Useful if you've just received an email that says it has attachments but you can't get them out (as I just did!).  View the raw source of the email, copy the Base64 encoded text, drop in to a file, and run through this.  The output will be the binary (or ascii) attachment.

    perl -MMIME::Base64 -ne 'print decode_base64($_)' < file.txt > out