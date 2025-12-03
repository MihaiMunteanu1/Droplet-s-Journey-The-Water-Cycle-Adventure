# **Documentație de Proiectare Finală: "Aventura Picăturii"**

Data: 21 Noiembrie 2025

## **I. Viziunea Proiectului**

**"Aventura Picăturii"** este o aplicație desktop educativă destinată copiilor de grupă mare (5-6 ani). Proiectul transformă lecția clasică despre circuitul apei în natură într-o experiență interactivă, narativă și ludică.

Copilul nu doar privește, ci participă activ la fiecare etapă a procesului natural, având rolul de a ajuta elementele naturii (soarele, norii, apa) să își îndeplinească funcția. Scopul final este înțelegerea cauzalității: căldura evaporă apa \-\> vaporii formează nori \-\> norii aduc ploaia \-\> ploaia umple râurile.

## **II. Specificații Tehnice și Design**

### **1\. Context Tehnic**

* **Platformă:** Aplicație Web/Desktop (rulată în browser, compatibilă Windows/macOS).  
* **Tehnologii:** HTML5, CSS3 (pentru animații fluide și stilizare), JavaScript (pentru logica jocului).  
* **Grafică:** Vectorială (SVG) pentru claritate maximă pe orice rezoluție, folosind un stil artistic "flat", prietenos și colorat.

### **2\. Audiență și Accesibilitate**

* **Public Țintă:** Copii 5-6 ani.  
* **Stil Vizual:** Culori vii, forme rotunjite, elemente mari și clare.  
* **Feedback:** Vizual (schimbări de culoare, animații de succes) și text simplu pentru instrucțiuni.

### **3\. Interacțiune**

* **Input Primar:** Mouse (Drag & Drop, Click & Hold, Click simplu).  
* **Interfață:** Minimalistă. Include o bară de progres sus pentru a motiva copilul și instrucțiuni clare (toasts) în partea de jos a ecranului.

## **III. Descrierea Detaliată a Scenariului (Gameplay)**

Aplicația este structurată secvențial în 4 scene interactive, plus un ecran de start și unul de final.

### **Scena 1: Evaporarea**

* **Context:** Un peisaj marin cu cer senin și un soare strălucitor.  
* **Obiectiv:** Încălzirea apei mării pentru a crea vapori.  
* **Mecanică:** **Drag & Drop**. Copilul trebuie să tragă soarele din colțul ecranului și să îl poziționeze aproape de linia apei.  
* **Feedback:** Când soarele este poziționat corect (jos), apar animații ondulate care sugerează evaporarea ("aburi"), iar soarele strălucește mai puternic.

### **Scena 2: Condensarea**

* **Context:** Cerul albastru unde vaporii trebuie să se adune.  
* **Obiectiv:** Formarea unui nor de ploaie prin colectarea picăturilor de apă evaporate.  
* **Mecanică:** **Drag & Drop (Colectare)**. Pe ecran apar 6 picături de apă dispersate. Copilul trebuie să le tragă pe rând în interiorul unui contur de nor punctat.  
* **Feedback:** Pe măsură ce picăturile sunt adăugate, conturul norului reacționează (flash alb). Când toate cele 6 picături sunt colectate, norul devine solid, pufos și primește o față veselă.

### **Scena 3: Precipitațiile**

* **Context:** Un peisaj montan impunător, cu un nor mare pe cer.  
* **Obiectiv:** Declanșarea ploii pentru a umple rezervoarele naturale de apă.  
* **Mecanică:** **Click & Hold (Ține apăsat)**. Copilul trebuie să țină click apăsat pe nor.  
* **Feedback Vizual:**  
  * Cât timp este apăsat, norul și cerul se întunecă (simulând furtuna).  
  * Începe o animație de ploaie care cade peste munte.  
  * În dreapta ecranului, un "rezervor" gradat arată vizual cantitatea de apă din nor scăzând (sau acumulându-se jos), învățând copilul despre volum și durată.

### **Scena 4: Colectarea și Curățarea**

* **Context:** Un râu care curge printr-o câmpie verde, dar cursul apei este blocat de pietre.  
* **Obiectiv:** Curățarea albiei râului pentru ca apa să poată ajunge înapoi în mare (închiderea circuitului).  
* **Mecanică:** **Click (Acțiune rapidă)**. Spre deosebire de primele scene, aici interacțiunea este de tip "curățare". Copilul dă click pe cele 5 pietre care blochează râul.  
* **Feedback:** La click, pietrele se micșorează și dispar (efect "pop"), eliberând vizual cursul apei. Când toate pietrele sunt eliminate, apa curge liberă.

### **Final**

* Ecran de felicitare cu un mesaj pozitiv ("Ai completat Circuitul Apei\!") și buton de "Rejoacă", încurajând repetiția pentru fixarea cunoștințelor.

## **IV. Elemente Tehnice Specifice Implementate**

1. **Grafică SVG Scalabilă:** Toate elementele (nori, soare, munte, picături) sunt desenate direct în cod folosind SVG. Acest lucru asigură că jocul arată perfect clar pe orice ecran, de la laptopuri mici la monitoare mari, fără pixelare.  
2. **Sistem de Particule Simplificat:** Pentru ploaie și aburi s-au folosit animații CSS și SVG (\<animate\>) care rulează fluid fără a îngreuna procesorul.  
3. **Gestionarea Stării (State Management):** Aplicația ține minte progresul în timp real (câte picături au fost adunate, cât timp a plouat, câte pietre au fost curățate) pentru a trece automat la nivelul următor doar când sarcina este completă.



<img width="2363" height="1467" alt="Screenshot 2025-11-21 104705" src="https://github.com/user-attachments/assets/c2006a01-7199-4c63-8a1f-2e11110da5cb" />
<img width="2285" height="1464" alt="Screenshot 2025-11-21 104714" src="https://github.com/user-attachments/assets/638a517d-8334-4877-8d1b-aa8191418acd" />
<img width="2278" height="1437" alt="Screenshot 2025-11-21 104727" src="https://github.com/user-attachments/assets/8d92c69f-4d34-4713-ac61-2c0ff4f33790" />
<img width="2284" height="1441" alt="Screenshot 2025-11-21 104743" src="https://github.com/user-attachments/assets/0a471e89-9b9a-4071-8264-e058110d99d4" />
<img width="2228" height="1447" alt="Screenshot 2025-11-21 104759" src="https://github.com/user-attachments/assets/39a0dd84-2084-4bfc-98c5-3212f2734ff9" />
<img width="2183" height="1447" alt="Screenshot 2025-11-21 104810" src="https://github.com/user-attachments/assets/1ba8f52e-9ee5-4ad8-b2bb-4240b52e4c40" />




