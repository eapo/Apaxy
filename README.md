# Custom FancyIndexing

Demo: [hej.valto.ro/brand/data/](https://hej.valto.ro/brand/data/)

Custom FancyIndexing is a customisable theme built to enhance the experience of browsing web directories. It uses the `mod_autoindex` Apache module—and some CSS—to override the default style of a directory listing.

## Features

Custom FancyIndexing may be basic, but it gives you a great deal of creative freedom when styling your directory.

* Style your directory listing with CSS.
* Make it pop with Javascript or jQuery.
* Add welcome messages, download instructions or copyright notices.
* Add custom mime type icons (requires editing the `.htaccess` file)
* SVG icons using FontAwesome Sprites

## Installation

Apaxy requires an Apache(2.2.11+) enabled HTTP server.

Let's assume you have a folder named `data` in your server root directory (the path thus being `http://mywebsite.com/data`) that you'd like to use as your listing directory:

1. [Download](https://github.com/eapo/Custom-FancyIndexing/archive/master.zip) and unzip
2. Copy and paste the contents of the `/apaxy` folder to your `/data` folder.
3. Rename `htaccess.txt` to `.htaccess` in both the `/share` and `/share/theme` folders.
4. [Treat yo'self](https://media.tenor.com/xrldoiZ-bgEAAAAC/bear-dance.gif), you're done.

## Docker images

A [local Demo](http://localhost:8080) can be started with docker.
`docker-compose build`
`docker-compose up`

## Custom FancyIndexing themes

If you'd like to alter the default Custom FancyIndexing theme, look in the `/theme` folder and you'll find the following files:

* `header.html`
* `footer.html`
* `style.css`

Edit these as you would any other HTML or CSS file.

Adding your own icons is a little more involved. You'll need to edit the main Custom FancyIndexing `.htaccess` file. Look for the following as an example:

    AddIcon (PDF,/data/theme/svg.php?q=file-pdf) .edn .pdf

The above rule will 
* assign a FontAwesome icon named `file-pdf` 
* from the FontAwesome sprite file `theme/solid.svg` 
* set in the `theme/svg.php` 
* to any file with the `.edn` and `.pdf` extensions,
* with the alternate name of *"PDF"* for the images.

This URL path is relative to your site's root.

## Mime Types

The default Apaxy theme `theme/apaxy` has icons in place for the following mime types:

    .7z .aac .ai .aif .aifc .aiff .ape .asf .asx .au .avi .bat .bin .bmp .bz2 .c .cab .cmd 
    .cpp .css .csv .deb .dmg .doc .docm .docx .dot .dotm .dotx .edn .eps .exe .f4a .f4b .f4p 
    .f4v .flac .flv .gif .gz .h .hex .htm .html .ico .iff .iso .it .jar .jpe .jpeg .jpg .js 
    .json .log .m3u .m3u8 .m4a .m4v .md .mid .mkv .mod .mov .mp3 .mp4 .mpa .mpg .msg .nfo 
    .odt .oga .ogg .ogv .pages .pdf .php .phtml .pkg .pls .pls8 .png .ps .psd .py .ra .rar 
    .rb .rm .rpm .rss .rtf .s3m .sass .scss .sh .shtml .sql .srt .svg .svgz .swf .tar .tex 
    .tif .tiff .txt .URL .url .vob .wav .wma .wmv .wpd .wps .xhtml .xlam .xlr .xls .xlsm 
    .xlsx .xltm .xltx .xm .xml .zip 

## Credits

Custom FancyIndexing owes it's existence to [Apaxy](https://github.com/AdamWhitcroft/Apaxy/) by [@adamwhitcroft](https://twitter.com/adamwhitcroft) and [Font Awesome](https://fontawesome.com/)
