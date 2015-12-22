## Installing linter for emacs:

1. install melpa by adding these lines into your .emacs file:
	
		(require 'package) ;; You might already have this line
		(add-to-list 'package-archives
		             '("melpa" . "http://melpa.org/packages/") t)
		(when (< emacs-major-version 24)
		  ;; For important compatibility libraries like cl-lib
		  (add-to-list 'package-archives '("gnu" . "http://elpa.gnu.org/packages/")))
		(package-initialize) ;; You might already have this line


2. then restart emacs then type, M-x package-install RET flycheck

3. Install cask, by typing: 

		curl -fsSL https://raw.githubusercontent.com/cask/cask/master/go | python

4. then add these line in your cask file:

		(source gnu)
		(source melpa)
		(depends-on "flycheck")

5. then in .emacs file add

		(add-hook 'after-init-hook #'global-flycheck-mode)

