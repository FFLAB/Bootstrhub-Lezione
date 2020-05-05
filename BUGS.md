BUGS IN BOOTSTRAP/JQUERY

Non funziona dropdown menu hamburger:
collapse.js:346 Uncaught TypeError: Cannot convert object to primitive value

Solution in https://github.com/twbs/bootstrap/issues/30553
alazark94 commented 23 days ago • 
in node_modules/bootsrap/dist/js/bootstrap.js line 1509 change

if (!data && _config.toggle && /show|hide/.test(config))

to

if (!data && _config.toggle && /show|hide/.test(_config))

or use jquery 3.4.1 until twbs/bootstrap#30553 is fixed
eseguito:
npm install jquery@3.4.1 --save
(alternativa usare cdn https://cdnjs.cloudflare.com/ajax/libs/jquery/3.4.1/jquery.min.js)

Errori in console di Popper.js:
Tramite <script> bisogna caricare il file nella cartella dist/umd/popper.min.js