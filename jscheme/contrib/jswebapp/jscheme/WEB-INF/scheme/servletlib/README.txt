The scheme files in this folder are loaded into the execution environment of the scheme servlet handler.
They define the following procedures (listed by file in which the definitions appear)

  files.scm          ; (write-to-file F D) (append-to-file F D) (read-from-file F D) (read-all-from-file N D) (read-string-from-file N D) (servlet-file request N)
  forms.scm          ; (make-form url . args)
  getformvalues.scm  ; (get-form-values request x)
  servlet.scm        ; (servlet vars . body) (basic-webpage title body) (warning-webpage body)
  session.scm        ; (session-set request name value) (session-get request name default)
  tables.scm         ; (ol L) (ul L) (lis L) (table Rows) (trs Rows)
  applets.scm        ; (applet request width height file) (multi-jar-applet request W H F)
  redirect.scm       ; (redirect response relativeurl)
  graphics.scm       ; (send-jpg response w h drawfn)
  view.scm           ; (viewCode file) 

The following three are not loaded by default and you
must explicitly configure these to work with your system
(i.e. provide mail server and database server urls, passwords, etc.)

; mail.scm           ; (send-mail request to from subj text)
; db.scm             ; database jdbc-driver jdcb-driver-class (connect host/db user pw) (handlequery con query) (runquery host/db user pw) (toMYSQL x) (toHSQL x) (toSQL x)
; db.hide            ; (open-dbconnection) dbconnection dbquery
