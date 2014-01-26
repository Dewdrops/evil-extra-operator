English is not my first language, so feel free to correct me of any mistake.

evil-extra-operator
===================

Evil operator for evaluating codes, translating text, taking notes, searching via google, etc.


Installation
------------

```lisp
;; change default key bindings (if you want) HERE
;; (setq evil-extra-operator-eval-key (kbd "ge"))
(require 'evil-extra-operator)
(global-evil-extra-operator-mode 1)
```
The key binding customization must be placed BEFORE `(require 'evil-extra-operator)`.


Commands and default bindings
-----------------------------

`gr` (evil-operator-eval)

Operator for evaluating code, i.e., use `grip` to evaluate current paragraph, `grr` to evaluate current line, or if you are in visual state, `gr` to evaluate current active region.
You can customize option `evil-extra-operator-eval-modes-alist` to let evil-operator-eval support more language. Example:
```lisp
(setq evil-extra-operator-eval-modes-alist
  '((ruby-mode ruby-send-region)
    (enh-ruby-mode ruby-send-region)))
```
See document for this option for details.

---

`gG` (evil-operator-google-search)

Operator to search the web via google.

---

`g.` (evil-operator-google-translate)

Operator to translate text via google translate.
To use this command, you should have [google-translate](https://github.com/manzyuk/google-translate) installed.

---

`gh` (evil-operator-highlight)

Operator to highlight region.
To use this command, you should have [highlight.el](http://www.emacswiki.org/emacs-en/download/highlight.el) installed.
You can use `hlt-eraser-mouse` or `hlt-eraser` which are provided by highlight.el to disable highlight

---

`gs` (evil-operator-fold)

Operator to fold region.
To use this command, you should have [fold-this.el](https://github.com/magnars/fold-this.el) installed.
You can use `fold-this-unfold-at-point` or `fold-this-unfold-all` which are provided by fold-this.el for unfolding.

---

`go` (evil-operator-org-capture)

Operator form of org-capture.
So you can use `goip` to capture current paragraph.

---

`gR` (evil-operator-remember)

Like evil-operator-org-capture, but use remember-region instead of org-capture.


See also
-----------------------------
[tarao](https://github.com/tarao)'s [evil-plugins](https://github.com/tarao/evil-plugins) provides operator for comment and moccur.
