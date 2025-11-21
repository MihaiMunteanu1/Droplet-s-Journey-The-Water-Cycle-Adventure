Documentație de Proiectare: Aplicație Educațională "Aventura Picăturii"

Echipa: Grupa 234
Curs: IOC 2025-2026
Data Actualizării: 21 Noiembrie 2025

I. Descriere Generală

"Aventura Picăturii" este o aplicație desktop interactivă destinată copiilor de 5-6 ani (grupa mare), având ca scop educarea acestora cu privire la circuitul apei în natură. Aplicația combină elemente narative cu mecanici simple de joc (Drag & Drop, Click), oferind un mediu de învățare "fără eșec", plin de feedback vizual și auditiv.

1. Specificații Tehnice

Platformă: Web / Desktop (rulată în browser).

Tehnologii: HTML5, CSS3, JavaScript (Vanilla).

Grafică: SVG (Scalable Vector Graphics) pentru redare clară pe orice rezoluție.

Stil: "Flat design", culori vii, forme prietenoase.

II. Structura Aplicației (Scene și Mecanici)

Aplicația este împărțită în 4 scene secvențiale, plus ecrane de start și final.

Scena 1: Evaporarea

Obiectiv: Încălzirea apei mării.

Mecanică: Drag & Drop. Copilul trage soarele aproape de apă.

Feedback: Apar aburi (animație SVG) când soarele este poziționat corect.

Scena 2: Condensarea

Obiectiv: Formarea norului.

Mecanică: Drag & Drop. Copilul trage 6 picături de apă într-un contur de nor.

Feedback: Conturul norului reacționează la fiecare picătură. La final, norul devine solid și pufos.

Scena 3: Precipitațiile

Obiectiv: Declanșarea ploii pe munte.

Mecanică: Click & Hold (Ține apăsat). Copilul apasă pe nor.

Feedback: Cerul se întunecă, norul devine gri, începe ploaia, iar un indicator ("Apă în Nor") arată progresul.

Scena 4: Colectarea (Curățarea Râului)

Obiectiv: Deblocarea cursului apei către mare.

Context: Un râu blocat de 5 pietre mari.

Mecanică: Click (Apasă). Copilul dă click pe pietre pentru a le elimina.

Feedback: Pietrele dispar cu o animație de micșorare și estompare ("pop"). Când toate sunt eliminate, apa curge liber.

III. Implementare Tehnică - Focus pe Scena 4

Această secțiune detaliază implementarea specifică a scenei finale, unde mecanica a fost schimbată din "Drag" în "Click" pentru o experiență mai fluidă.

1. Structura SVG (Vizual)

Scena este construită folosind elemente SVG suprapuse:

Fundal: Rectangul verde (#8bc34a) cu textură de iarbă (pattern).

Vegetație: Simboluri reutilizabile (<use>) pentru frunze (#leaf) și smocuri de iarbă (#grassTuft), rotite și scalate aleatoriu.

Râu: Două căi (path):

#s4-bed: Albia râului (culoare nisipie).

#s4-water: Apa (albastru), care include o animație de curgere (stroke-dashoffset) activată la final.

Pietre: Grupuri <g> cu clasa .poppable, conținând formele pietrelor.

2. Stiluri CSS (Animații)

Pentru a crea efectul de dispariție, folosim tranziții CSS pe proprietățile opacity și transform.

/* Clasa pentru pietrele interactive */
.poppable {
    cursor: pointer;
    transition: transform 0.2s, filter 0.2s; /* Animație la hover */
    transform-origin: center center; /* Scalare din centru */
}

/* Efect la trecerea mouse-ului */
.poppable:hover {
    transform: scale(1.1);
    filter: brightness(1.2);
}

/* Efectul de dispariție (aplicat prin JS) */
/* Notă: Aceasta se aplică direct pe element prin style.opacity și style.transform */


3. Logica JavaScript (Interacțiune)

Funcția cleanRock(element) gestionează interacțiunea. Este atașată direct pe elementele SVG (onclick="cleanRock(this)").

Codul Funcțional:

let rocksCount = 0; // Contor pentru pietrele curățate

function cleanRock(element) {
    // 1. Prevenim click-ul dublu
    if(element.classList.contains('cleaned')) return;
    element.classList.add('cleaned');
    
    // 2. Aplicăm animația de dispariție
    element.style.transition = "opacity 0.6s ease, transform 0.6s ease";
    element.style.opacity = '0';
    
    // Calculăm scalarea curentă pentru a micșora de la dimensiunea actuală
    // (Simplificat: adăugăm scale(0.3) la transformarea existentă)
    // Notă: În implementarea reală, suprascriem transform cu o valoare hardcoded sau calculată
    // pentru a evita conflictele de string-uri, dar efectul vizual este de "shrink".
    const currentTransform = element.getAttribute('transform');
    element.style.transform = `${currentTransform} scale(0.3)`;
    
    // Dezactivăm interacțiunea viitoare
    element.style.pointerEvents = 'none';
    
    // 3. Ascundem elementul complet după terminarea animației (opțional, pentru performanță)
    setTimeout(() => {
        element.style.display = 'none';
    }, 600);

    // 4. Actualizăm starea jocului
    rocksCount++;
    document.getElementById('msg-4').textContent = `Curăță pietrele din râu! (${rocksCount}/5)`;

    // 5. Verificăm condiția de victorie
    if(rocksCount >= 5) {
        // Pornim animația apei
        document.getElementById('s4-anim').beginElement();
        
        // Mesaj final și buton de continuare
        document.getElementById('msg-4').textContent = "Râul curge liber!";
        setTimeout(showNextButton, 1500);
    }
}


IV. Concluzii și Evoluție

Proiectul a evoluat de la schițe statice la un prototip funcțional complet. Decizia de a simplifica interacțiunea în ultima scenă (de la Drag & Drop la Click) a fost luată pentru a oferi o satisfacție imediată ("gratificare instantanee") la finalul jocului, simulând curățarea rapidă și eficientă a mediului înconjurător.
