# option 1 - making the macro
Make a new macro in solidworks

<img width="491" height="243" alt="image" src="https://github.com/user-attachments/assets/4c8c1d2f-8032-45d6-863c-048db38edca4" />

past the code from this repo.


# option 2 - saving the macro
download the file from this repo and save it on your pc

# adding the button 
right click the toolbar and click customize
<img width="641" height="254" alt="image" src="https://github.com/user-attachments/assets/6cd6c9ff-5cf3-48da-bffe-4bc13be32fc0" />

go to the commands tab and search for 'macro's'.

<img width="1005" height="445" alt="image" src="https://github.com/user-attachments/assets/4533be01-0c61-42eb-929c-891f45200463" />

drag the macro button to the toolbar and upon letting it go there a prompt opens. 
point the prompt to your macro save location

<img width="386" height="406" alt="image" src="https://github.com/user-attachments/assets/d29ba43c-cd79-4b04-8c74-abb4cd4f5652" />

push the button!


# trouble shooting.


## 1. Melding: “Kon SolidWorks niet bereiken.”
Oorzaak: De macro draait buiten SolidWorks of SolidWorks reageert niet.
Oplossing: Start altijd vanuit SolidWorks → Tools → Macro → Run…. Zorg dat SolidWorks actief is en er een document geopend is.

## 2. Melding: “Geen document geopend.”
Oorzaak: Er staat geen bestand open.
Oplossing: Open een Part (.sldprt) of Assembly (.sldasm).
Let op: Deze macro werkt niet met tekeningen (.slddrw).

## 3. Melding: “Alleen PART of ASSEMBLY kan naar STEP worden geëxporteerd (geen Drawing).”
Oorzaak: Je hebt een tekening geopend.
Oplossing: Sluit de tekening en open een Part of Assembly.

## 4. Melding: “Het document is nog niet opgeslagen. Sla eerst op als .sldprt of .sldasm.”
Oorzaak: Het bestand is nog niet eerder opgeslagen, dus de macro kent de map niet.
Oplossing: Sla het bestand handmatig op (File → Save As) voordat je de macro start.

## 5. Melding: “Export naar STEP is mislukt. Error code: … Warning code: …”
Oorzaak: SolidWorks heeft de export afgebroken. Mogelijke redenen:
Geen schrijfrechten in de doelmap.
De bestandsnaam is te lang of bevat speciale tekens.
SolidWorks exportmodule (STEP) niet geïnstalleerd/licentieprobleem.

Oplossing:
Probeer opslaan in een simpele map (bijv. C:\Temp).
Verander de naam van het bestand zodat er geen spaties of vreemde tekens in zitten.
Controleer of je handmatig via File → Save As → STEP kunt exporteren. Als dit ook niet lukt, ligt het aan SolidWorks zelf.

## 6. Bestand wordt niet overschreven
Oorzaak: Als er al een bestand met dezelfde naam bestaat, kan SolidWorks vragen om bevestiging. De late-binding macro overschrijft standaard alleen als SolidWorks dit toestaat.
Oplossing: Verwijder oude STEP-bestanden handmatig of breid de macro uit met een optie om automatisch te overschrijven.

## 7. Bestand wordt als .step of .stp opgeslagen?
Oorzaak: Verschillende systemen hanteren andere extensies.
Oplossing: In de code ".step" aanpassen naar ".stp" als dat nodig is.
