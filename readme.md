# Fira Code Symbol Mode

If you are a [FiraCode](https://github.com/tonsky/FiraCode) fan, you probably want to use its beautiful Symbols in coding as well. This can be done with Fira Code Symbol Minor Mode.

![demo](./demo/demo.gif)

Fira Code Symbols can help your code more readable.

## Prerequisite

install [Fira Code Symbol font](https://github.com/tonsky/FiraCode/files/412440/FiraCode-Regular-Symbol.zip) made by [@siegebell](https://github.com/siegebell)  

### Optional

additionally, you can install *prettify-greek* from Melpa for greek symbols  
Fira Code Symbol Minor Mode will automatically enable it with no further configuration

---

## Install

~~~scheme
(require 'fira-code-symbol)
~~~

put `fira-code-symbol.el` into  your load-path & add the above code in your init.el file

---

## Enable Fira Code Symbol in current buffer

~~~scheme
M-x fira-code-symbol-mode
~~~

enable / disable Fira Code Symbol Minor Mode in current buffer

---

## Enable Fira Code Symbol by add-hook

~~~scheme
(add-hook 'python-mode-hook 'fira-code-symbol-hook)
~~~

enable Fira Code Symbol Minor Mode mode in python major mode automatically

---

## Enable Fira Code Symbol in current Major Mode

~~~scheme
M-x enable-fira-code-symbol-in-major-mode
~~~
enable Fira Code Symbol Minor Mode in all buffers opened in current major mode & add hook to the current major mode's hook

---

## Disable Fira Code Symbol in current Major Mode

~~~scheme
M-x disable-fira-code-symbol-in-major-mode
~~~
disable Fira Code Symbol Minor Mode in all buffers opened in current major mode & remove hook from the current major mode's hook  
You should know that this function will remove fira-code-symbol-hook from `prog-mode-hook`(if it has) as a side effect

---

## Global Fira Code Symbol (not recommended)

~~~scheme
(global-fira-code-symbol-mode 1)
~~~

enable Fira Code Symbol Minor Mode globally, It's probably not a good idea to have  Fira Code Symbol in a major mode like org-mode.
