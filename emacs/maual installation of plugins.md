Manual Installation of plugin in emacs
=====================================

### Type in Emacs

`M-x eshell`

`wget <url of package>`

### extrack the file
`tar xjf <dir/xxx.tar.gz>`


### load file into install
`M-x load-file [enter]`
<type the location of the extracted file untill install.el> ex. `/<package>/etc/install.el` [enter]
install to
./emacs/d [enter]


### copy and paste code like:
	(add-to-list 'load-path "~/.emacs.d/")
	(require 'auto-complete-config)
	(add-to-list 'ac-dictionary-directories "~/.emacs.d//ac-dict")
	(ac-config-default)


### then type in the buffer
`M-x eval-buffer [enter]`
