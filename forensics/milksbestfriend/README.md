Fun little JPEG challenge.

Steps:
Downloaded File and ran exiftool, aperisolve, nothing interesting
Found an interesting string with xxd "This is not the flag you are looking for."
Looked into JPEG encoding. FFD9 marks end of image. This is actually in the middle of the
file, directly followed by something like "Rar!" in the binary.

Used dd to extract the second part of the file (which we expect to be a rar) and stored it in a rar.
Extracted it -> Image with two Oreos!

xxd again and we have the flag.
