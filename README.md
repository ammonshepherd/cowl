# Description:

cowl is a program that will take a directory of images and do the following actions on each image: 
    1) create a copy of the image with a watermark, 
    2) OCR the image and create a txt file containing the text, 
    3) compile the images into a single PDF document.



# Usage: 

cowl [options]


# Options:

    -i, --input                      Specify the directory where the images are found.

    -l, --lang                       Set the language for the OCR program to use. This is the language used in the documents. Default is German.

    -m, --mark                       Set the text to be used in the water mark.

    -o, --output                     Set the directory name where the watermark and OCR files are output.

    -h, --help                       Show this help message.
