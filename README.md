# Usage: 

    cowl [options]

cowl is a program that will take a directory of images
and do the following actions on each image by default: 
1. create a copy of the image with or without a watermark, 
2. OCR the image and create a txt file containing the text, 
3. compile the images into a single PDF document.

Optional parameters exist to change and/or turn off certain behaviors.

# Options:

    -c, --cleanup                    Delete images and folders created by running this script.

    -d [/path/to/directory],         Specify a directory where the watermarked
        --dir-out                       images and OCR files are created. 

    -i [/path/to/directory],         Specify the directory where the images are found.
        --dir-in

    -l, --lang                       Set the language for the OCR program to
                                        use. This is the language used in the
                                        documents. Default is German [:deu].

    -n, --no-watermark               Don't do the watermark thing.

    -o, --no-ocr                     Don't run the OCR software on the image.

    -p, --no-pdf                     Don't create a PDF of all images.

    -t, --text [TEXT]                Set the text to be used in the water mark.

    -w, --watermark [/path/to/image] Specify the image to use for the watermark

    -h, --help                       Show this help message.


# Set up

This assumes you already have ruby and rubygems installed.

Download the repo in your home directory:

    git clone https://github.com/mossiso/cowl

This creates a folder called cowl and put three files into it. Now change directories into the cowl directory.

    cd cowl

Get the required gems by running bundler.

    bundle

Edit the cowl file to change the default copyright text. Change the line:

    options.mark_text = "Copyright ©2014 The Marvellous and awesome Me" # TODO: get date from image file                                                  

# Examples

In your terminal program, enter into the directory where you have images.

    cd /path/to/images/

Run the cowl command

    ruby /home/billy/cowl

Running without any options will create a copy of the images, OCR them, put a
watermark on the copies, and combine them all into on PDF. 

The default text for the watermark is hard coded in the cowl script. You can change it there, or use the -t option.

    ruby /home/billy/cowl -t "Copyright ©2015 Billy Jorgenson Photography"

To change the language used in the OCR to English

    ruby /home/billy/cowl -l eng
