\# Task 2 - Image Scaling using FFmpeg



This task involves preprocessing dataset images by resizing them to a lower resolution while maintaining aspect ratio using FFmpeg.



\## Objective

To reduce image dimensions for efficient model training while preserving the aspect ratio of objects in the dataset.



\## Process Followed



\- The dataset images were divided into train, validation, and test sets.

\- All images were resized using FFmpeg.

\- The aspect ratio was preserved using a fixed width of 384 pixels and automatic height adjustment (-1).

\- The same filenames were retained after resizing.



\## Command Used



ffmpeg command used for resizing images:



ffmpeg -i input.jpg -vf scale=384:-1 output.jpg



Batch processing was done using PowerShell to apply the same operation to all images in train, val, and test folders.



\## Output



\- scaled\_train: resized training images

\- scaled\_val: resized validation images

\- scaled\_test: resized test images



All images are scaled to width 384 while maintaining aspect ratio.



\## Result



The dataset is now optimized for model training with reduced image size, improving processing efficiency while preserving visual integrity.

