# prg8--week5-herkansing
herkansing van programmeren 8 opdracht week 5

Welk model heb je gebruikt ? (handpose, facepose, bodypose)
ik heb de handpose gebruikt voor deze opdracht.

Welk model heb je gebruikt ? (handpose, facepose, bodypose)
Het model had verschillende handsignalen moeten herkennen zoals: duim omhoog/omlaag, peace teken en bijvoorbeeld een middelvinger

Is het jou gelukt om de pose data uit te lezen in de console, en de data geschikt te maken om mee te trainen? Hoe heb je dit gedaan?
De functie predictLandmarks roept het model aan om de locatie van de vingers in de video te voorspellen en slaat de voorspelling op in de predictions-variabele.
De functie logData wordt aangeroepen met de predictions-array als argument. Binnen deze functie wordt eerst een eventlistener toegevoegd aan de knoppen "buttonA" en "buttonB" om de trainingsgegevens vast te leggen.
De landmarks van de voorspelling worden omgezet naar een 1D-array van predictionsArray met behulp van de reduce-methode. Elke x- en y-coördinaat van de landmarks wordt afzonderlijk toegevoegd aan de array.
Met behulp van de KNN-classificator (machine) wordt de predictionsArray geleerd met de learn-methode.
Vervolgens wordt de pose voorspeld met de classify-methode van de KNN-classificator en wordt de voorspelde pose gelogd in de console en weergegeven in de HTML in het element met de id "array".

Is het jou gelukt om middels HTML buttons de train functie van KNN aan te roepen met pose data? Geef aan wat je hier makkelijk of moeilijk aan vond.
De trainingsfunctie wordt gedefinieerd als buttonAHandler en buttonBHandler.
Bij het laden van de pagina worden event listeners toegevoegd aan de knoppen "buttonA" en "buttonB", die de respectieve trainingsfuncties aanroepen wanneer erop wordt geklikt.
De trainingsfuncties (buttonAHandler en buttonBHandler) roepen de learn-methode van de KNN-classificator (machine) aan en geven de predictionsArray (pose data) en het bijbehorende label mee als argumenten.
In de console wordt het label (bijvoorbeeld "duim" of "high-five") gelogd.

Het moeilijke hiervan vond ik om de data op te kunnen slaan in een array en deze op de juiste manier te kunnen gebruiken voor het trainen.

Is het jou gelukt om via een button een voorspelling van pose data te kunnen doen? Klopte de voorspelling ook?
ja doormiddel van de aangemaakte knoppen kan ik nu een voorspelling doen van de gemaakte handgebaren, en deze voorspellingen kloppen ook!

Is je idee voor een applicatie uiteindelijk ook gelukt? Ben je tegen problemen aan gelopen? Zo ja, welke problemen, en wat was jouw aanpak om het op te lossen?
ja mijn applicatie kan zowel de duim omhoog als high five handgebaar herkennen, voor mij was het grootste probleem om de data op de juiste manier in een array te zetten, om dit op te lossen heb ik online videos bekeken en heb ik klasgenoten om hulp gevraagd.
