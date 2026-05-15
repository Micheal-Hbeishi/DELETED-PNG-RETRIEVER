JPEG Recovery Script

This Python script performs basic JPEG file carving from a raw drive or disk image by scanning for JPEG file signatures and extracting detected images.

Features
Scans a raw drive/device byte-by-byte in chunks
Detects JPEG headers (FFD8FFE0)
Detects JPEG end markers (FFD9)
Recovers and saves JPEG files automatically
Useful for introductory digital forensics and data recovery labs

How It Works
Opens a raw drive (G:) in binary read mode
Reads data in 512-byte sectors
Searches for the JPEG header signature:
FF D8 FF E0 00 10 4A 46
When found:
Creates a new .jpg file
Begins writing bytes to that file
Continues until the JPEG footer is found:
FF D9
Saves the recovered image into the 1/ directory

Example Output
Found JPEG header at location: 0x1f3400 =====
Wrote JPEG at location: 0.jpg =====
