---
title: "Assignment_3"
date: 2016-02-25
---

Zadanie:
Vytvorenie xml-schemy, ktora bude obsahovat elementy prezentacie, a vytvorenie xsl transformacii, ktore budu sluzit na 
transformaciu danych elementov do xhtml a pdf.  Sucastou je tiez vytvorenie xml prezentacie, ktora bude demonstrovat 
pouzitie elementov a danych transformacii.

Riesenie:
Boli vytvorene xml-schema elementy, ktore urcuju bud layout slajdu, alebo jeho obsah. Layout sa rozdeluje do panelov,
ktore rozdeluju panel, v ktorom sa nachadzaju vertikalne, alebo horizontalne. Takimto delenim priestoru sa docieli
genericky layout slajdu, namiesto mnoho obmedzujucich sablon layoutu. Elementy obsahu su klasicke list,tabulka,obrazok 
a paragraf, ktory moze navyse obsahovat inline elementy ako emphasis, italic, breakline.. Sucastou su tiez par metadatovych
elementov a atributov ako note, description atd. Transformacia do html berie kazdy slajd ako osobity subor, co sa dosiahlo
pomocou xslt 2.0 a tagu <resultdocument>. Xsl subory transformacie do html a pdf oba includuju subory s parametrami, ako napr.
titlefont a textcolor, a takisto includuju core.xsl ako subor spolocnych jadro transformacii. Css styl sa pouzil aj ako
interny text v hlavicke pouzitim elementu style a aj ako interny text v elementoch pouzitim atributu style.
