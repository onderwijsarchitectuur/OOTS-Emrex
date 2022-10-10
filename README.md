# OOTS-Emrex

(noot: dit model kan worden ingeladen en eventueel bewerkt met coArchi: https://github.com/archimatetool/archi-modelrepository-plugin)

In Europees verband wordt langs meerdere paden nagedacht op het bevorderen van studentmobiliteit: 

1. Emrex
   
   Emrex is een community met (vrijwillige) deelname uit 10+ lidstaten, tot stand gekomen met financiering van de EU  voor grensoverstijgende uitwisseling van diploma’s.  DUO stelt via dit netwerk 10 miljoen Nederlandse diploma’s ter beschikking, niet aan overheden of scholen, maar aan de diplomahouder zelf, die volledige regie heeft  over wat met wie wordt gedeeld. 
   
2. Once Only Technical System (OOTS)
   
   OOTS is een communicatieprotocol ontwikkeld door de EU voor grensoverstijgende verkeer. Niet alleen voor diploma's maar voor een groot aantal bewijstukken die relevant zijn voor 21 publieke procedures uit de SDG-verordening. In juni 2022 is OOTS wettelijk verplicht gesteld in een Implementing Act. Deze act stelt preview en consent centraal en noemt Emrex als voorbeeld van een sectoraal systeem om mee samen te werken.

In 2022 wordt door de EU en Emrex overlegd over synergie tussen beide. Deze repository loopt daar op voor uit. 

Schematisch zit het uitwisselingspatroon van Emrex er zo uit;

![Emrex](https://github.com/onderwijsarchitectuur/OOTS-Emrex/blob/master/OOTS-Emrex.png)

Dit patroon lijkt in hoofdlijnen op dat van een webwinkel en een bank. De klant bestelt een product in een webwinkel en wordt dan doorgeleid (redirect) naar een bank. Vervolgens geeft de klant, na te zijn ingelogd, een opdracht aan de bank om geld over te maken. Het is niet de webwinkel die de betaalopdracht geeft via een backchannel, maar de klant zelf via de frontoffice. Na de betaling wordt  de klant teruggeleid naar de webwinkel. Het idee van “preview en consent” werkt nmet zo en is operationeel in Emrex. Technische details: https://emrex.eu/technical/.

Stel dat een Nederlander zich digitaal inschrijft voor een opleiding in het hoger onderwijs in een ander land. Dat gebeurt doorgaans vai een digitale aanmeldapplicatie van de onderwijsinstelling (of zoals in Nederland collectief met Stuidielink). Gewenste input: vooropleidingen. Emrex stelt een open source plugin voor de aanmeldapplicatie beschikbaar.  De plugin, die eenvoudig kan worden geïntegreerd met den aanmeldapplicatie, ondersteunt het opzoeken van de diplomaprovider (DUO!) en de redirect naar duo.nl.  Na inloggen met DigiD kan de persoon zijn diploma’s inzien en na een expliciet akkoord (consent) wordt dit digitaal ondertekend en verstuurd naar de onderwijsinstelling. Achteraf kan DUO door logging aantonen dat toestemming is gegeven (eis AVG art 7.1). 

Het webwinkelpatroon kan worden toegepast voor alle typen bewijsstukken. Naast diploma’s  gaat het de EU in eerste instantie over werkervaring, kentekenregistraties, inkomens en gegevens van de bevolkingsadministratie. In plaats van iedere bronhouder apart te laten aansluiten kan het handig zijn om daarvoor een nationaal overheidsportaal te gebruiken.  Met op de achtergrond een realtime verbinding tussen het portaal en de bronhouders. Een nationaal portaal betekent niet dat alle gegevens fysiek in één database zitten.
