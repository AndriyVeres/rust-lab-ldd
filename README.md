# Rust Laboratory: Linux Device Drivers
Source code of the [Linux Device Drivers in Rust](https://www.rust-lab.org/ldd) book, hosted on [rust-lab.org](https://www.rust-lab.org/)
##### How to build a self-hosted version of book
###### Prerequisites:
1. [Rust language](https://rust-lang.org/tools/install/)
2. [mdBook](https://rust-lang.github.io/mdBook/guide/installation.html)
###### Building:
1. Clone this repository:
```
$ git clone https://github.com/AndriyVeres/rust-lab-ldd.git
$ cd rust-lab-ldd
```
2. There are several ways to render a book, but one of the easiest methods is to use the serve command, which will build your book and start a local webserver:
```
$ mdbook serve --open
```
The ```--open``` option will open your default web browser to view your new book. You can leave the server running even while you edit the content of the book, and mdBook will automatically rebuild the output and automatically refresh your web browser.

###### Hosting the rendered book:
1. Build the HTML+JS render of the book:
```
$ mdbook build
```
2. To host the book you need to install a web server on your's hosting machine. Here is a partial list of popular web server software:
	1. [Apache2](https://httpd.apache.org/)
	2. [nginx](https://nginx.org/)
	3. [lighttpd](https://www.lighttpd.net/)
3. Copy the content of **book** directory into webserver directory, for example in Apache2 web site is placed in **/var/www/**:
```
$ cd book
$ sudo cp -r ./* /var/www/path/to/website/
```
##### Contribution
Any useful changes for the book are welcome. Feel free to open the pull request with proposed changes.