## Installing jedi autocompete for emacs

Step 1:

     ;; So the idea is that you copy/paste this code into your *scratch* buffer,
     ;; hit C-j, and you have a working el-get.
     (url-retrieve
     "https://raw.githubusercontent.com/dimitri/el-get/master/el-get-install.el"
     (lambda (s)
     (goto-char (point-max))
     (eval-print-last-sexp)))

Step 2: Open emacs then type C-x C-f then .emacs and then paste:


     (add-to-list 'load-path "~/.emacs.d/el-get/el-get")

     (unless (require 'el-get nil 'noerror)
     (with-current-buffer
     (url-retrieve-synchronously
     "https://raw.githubusercontent.com/dimitri/el-get/master/el-get-install.el")
     (goto-char (point-max))
     (eval-print-last-sexp)))

     (add-to-list 'el-get-recipe-path "~/.emacs.d/el-get-user/recipes")
     (el-get 'sync)
    


then save `C-x C-s`



Step 3: type this in emacs:
     
      1. `M-x el-get-install RET jedi RET`      
      RET means Enter key
      next, go to .emacs then paste


```
      (add-hook 'python-mode-hook 'jedi:setup)
      (setq jedi:complete-on-dot t) 
```

then save
      
Step 4:
     install virtualenv, go to terminal then type
     1. `sudo pip install virtualenv`


Step 5:(final)
     type this in emacs:
     
     `M-x jedi:install-server`







