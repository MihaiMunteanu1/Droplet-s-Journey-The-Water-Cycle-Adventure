# **Propunere de Proiectare: Aplicație Educațională "Circuitul Apei în Natură"**

Echipa: Grupa 234  
Curs: IOC 2025-2026

## **I. Specificații Generale (Comune pentru ambele concepte)**

Aceste specificații tehnice și filosofii de design reprezintă fundația proiectului și se aplică indiferent de varianta de gameplay aleasă.

### **1\. Context Tehnic și Audiență**

* **Platformă:** Aplicație Desktop (Windows/macOS).  
* **Audiență:** Copii de grupă mare (5-6 ani).  
* **Stil Grafic:** Culori vii, prietenoase, design 2.5D sau 3D low-poly (forme simplificate). Paletă cromatică dominată de albastru, verde și galben.

### **2\. Interacțiune și Input**

* **Input Primar:** Mouse (Drag & Drop, Click), Butoane-Pictogramă mari (fără text).  
* **Input Secundar (Accesibilitate):** Comenzi vocale simple pentru navigare și acțiuni (ex: „Mergi”, „Sus”, „Ploaie”).  
* **Interacțiune Duală:** Orice acțiune critică poate fi realizată atât prin click, cât și vocal.

### **3\. Filosofia de Design**

* **Mediu "Fără Eșec":** Aplicația încurajează explorarea. Greșelile nu sunt pedepsite, ci corectate printr-un feedback blând și amuzant.  
* **Feedback Auditiv:** Sunete clare pentru fiecare interacțiune (clipocit de apă, fâșâit de vânt, sunete cristaline pentru succes).  
* **Narațiune Ghidată:** Un personaj sau un narator este mereu prezent pentru a oferi context, eliminând nevoia de a citi text.

## **II. Concept A: "Aventura Picăturii Strop"**

Tip: Joc Narativ / Platformer (Story-driven)  
Perspectiva: Micro (Copilul este parte din proces)

### **1\. Viziunea Proiectului**

„Aventura Picăturii Strop” este o călătorie interactivă în care copilul urmărește și controlează un personaj simpatic – o picătură de apă numită „Strop”. Scopul este parcurgerea secvențială a etapelor circuitului apei, experimentând transformările fizice ale apei "pe propria piele".

### **2\. Elemente Centrale**

* **Hub-ul Central:** Un peisaj viu care se mișcă ușor, înlocuind meniul static. Copilul alege locația pentru a începe povestea (Mare, Cer, Munte).  
* **Personaj:** "Strop" – o picătură cu ochi expresivi care vorbește cu copilul („Brr, m-am răcit\!” sau „Mă simt ușor ca un balon\!”).

### **3\. Gameplay și Mecanici pe Etape**

Aplicația este împărțită în 4 scene secvențiale:

* **Scena 1: Evaporarea (Marea și Soarele)**  
  * *Obiectiv:* Încălzirea apei pentru a se ridica la cer.  
  * *Acțiune:* Drag & Drop cu razele soarelui peste apă. Comandă vocală: „Soare\!”.  
  * *Feedback:* Apar aburi zâmbitori care se ridică spre susul ecranului.  
* **Scena 2: Condensarea (Cerul și Norii)**  
  * *Obiectiv:* Formarea norilor.  
  * *Acțiune (Sortare):* Copilul adună „stropii gazoși” într-un singur loc până fac „Puf\!” și devin un nor.  
  * *Fără Eșec:* Dacă norul nu e gata, vaporii doar se împrăștie râzând.  
* **Scena 3: Precipitațiile (Muntele)**  
  * *Obiectiv:* Golirea norilor deasupra muntelui.  
  * *Acțiune:* Click & Hold pe nor pentru a-l „stoarce”. Joc de ritm pentru a crea fulgi de nea în zonele reci. Comandă vocală: „Plouă\!” sau „Ningă\!”.  
* **Scena 4: Colectarea (Râul și Întoarcerea)**  
  * *Obiectiv:* Ghidarea apei înapoi în mare.  
  * *Acțiune (Labirint):* Deblocarea drumului prin mutarea pietrelor/buștenilor (Drag & Drop).  
  * *Final:* Sărbătoare vizuală la reîntâlnirea cu marea.

## **III. Concept B: "Stația Meteo Magică"**

Tip: Joc de Simulare / Puzzle (Logic-driven)  
Perspectiva: Macro (Copilul privește lumea de sus, "God Game")

### **1\. Viziunea Proiectului**

Această abordare transformă copilul într-un „Mic Meteorolog” sau „Vrăjitor al Vremii”. Copilul nu mai controlează o picătură, ci întregul mediu, având acces la un panou de control prin care influențează fenomenele naturii pentru a rezolva probleme (ex: secetă, inundație).

### **2\. Elemente Centrale**

* **Vedere de ansamblu:** O planșă fixă cu un ecosistem complet (lac, munte, grădină) văzut de sus.  
* **Panoul de Comandă:** Situat în partea de jos, conține "ingredientele" vremii (Soare, Vânt, Frig, Căldură).  
* **Sarcina:** Rezolvarea unei probleme prin logică cauză-efect, nu prin parcurgerea unei povești liniare.

### **3\. Gameplay și Mecanici**

* **Mecanica de Combinații:** Copilul trebuie să combine elemente pentru a declanșa o reacție în lanț. Nu există buton direct de "Ploaie".  
  * *Algoritmul jocului:* Copilul trage „Soarele” peste „Lac” \-\> Se formează Norul \-\> Copilul trage „Frigul” peste „Nor” \-\> Începe Ploaia.  
* **Interacțiune Vocală:** Copilul dă ordine elementelor naturii: „Soare, încălzește\!”, „Vânt, suflă\!”.  
* **Recompensă Vizuală:** Transformarea mediului în timp real (iarba devine verde, florile cresc, nivelul râului crește).  
* **Eșec Amuzant (Trial & Error):** Dacă se aplică prea mult soare fără apă, iarba devine galbenă (dar se repară ușor aducând ploaia).

## **IV. Tabel Comparativ: Concept A vs. Concept B**

| Element | Concept A: "Aventura Picăturii" | Concept B: "Stația Meteo Magică" |
| :---- | :---- | :---- |
| **Tipul Jocului** | Narativ / Platformer (Story-driven) | Simulare / Puzzle (Logic-driven) |
| **Perspectiva** | **Micro** (Ești o picătură mică într-o lume mare) | **Macro** (Vezi toată lumea de sus, ca un uriaș) |
| **Obiectiv** | Să ajuți personajul să ajungă la finalul călătoriei. | Să menții echilibrul naturii (să uzi florile, să umpli râul). |
| **Mecanica** | Secvențială (Pasul 1 \-\> Pasul 2 \-\> Pasul 3). | Cauză-Efect (Dacă combin X și Y, rezultă Z). |
| **Feedback** | Personajul vorbește cu tine (emoțional). | Mediul se schimbă vizual (vizual/logic). |

* **Prima abordare (Concept A)** este emoțională și narativă, potrivită pentru copiii care învață prin povești.  
* **A doua abordare (Concept B)** este experimentală și logică, potrivită pentru copiii cărora le place să construiască și să vadă efecte.



<img width="2363" height="1467" alt="Screenshot 2025-11-21 104705" src="https://github.com/user-attachments/assets/c2006a01-7199-4c63-8a1f-2e11110da5cb" />
<img width="2285" height="1464" alt="Screenshot 2025-11-21 104714" src="https://github.com/user-attachments/assets/638a517d-8334-4877-8d1b-aa8191418acd" />
<img width="2278" height="1437" alt="Screenshot 2025-11-21 104727" src="https://github.com/user-attachments/assets/8d92c69f-4d34-4713-ac61-2c0ff4f33790" />
<img width="2284" height="1441" alt="Screenshot 2025-11-21 104743" src="https://github.com/user-attachments/assets/0a471e89-9b9a-4071-8264-e058110d99d4" />
<img width="2228" height="1447" alt="Screenshot 2025-11-21 104759" src="https://github.com/user-attachments/assets/39a0dd84-2084-4bfc-98c5-3212f2734ff9" />
<img width="2183" height="1447" alt="Screenshot 2025-11-21 104810" src="https://github.com/user-attachments/assets/1ba8f52e-9ee5-4ad8-b2bb-4240b52e4c40" />




