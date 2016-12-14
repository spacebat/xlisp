Change the working directory of your lisp image to the directory of the
exercise you want to work on, either by setting `*default-pathname-defaults*`
directly or if using the SLIME REPL, with the slime-cd command (at the REPL,
press `,` then `cd`). Then proceed to load the test file into your running Lisp
implementation, for example, `(load "point-mutations-test")`. This will run the
tests the first time automatically. After that you can run the test suite in
the REPL with `(lisp-unit:run-tests :all :point-mutations-test)`, and get more
usefully verbose information with:

```
(let ((*print-errors* t)
      (*print-failures* t))
  (run-tests :all :point-mutations-test))
```

## Making your first Common Lisp solution

To create lisp code that can be loaded with `(load "dna")`
for the first exercise, put this code in `dna.lisp`:

```lisp
(in-package #:cl-user)
(defpackage #:dna
  (:use #:common-lisp)
  (:export #:hamming-distance))

(in-package #:dna)

(defun hamming-distance (dna1 dna2)
  "Determine number of mutations between DNA strands by computing the Hamming Distance."
  )
```
