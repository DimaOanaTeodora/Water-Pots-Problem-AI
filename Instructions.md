:ballot_box_with_check:(5%)
   * :ballot_box_with_check: Fișierele de input vor fi într-un folder a cărui cale va fi dată în linia de comanda.
   * :ballot_box_with_check: În linia de comandă se va da și calea pentru un folder de output în care programul va crea pentru fiecare fișier de input, fișierul sau fișierele cu rezultatele.
   * :ballot_box_with_check: Tot în linia de comandă se va da ca parametru și numărul de soluții de calculat (de exemplu, vrem primele NSOL=4 soluții returnate de fiecare algoritm).
   * :ballot_box_with_check: Ultimul parametru va fi timpul de timeout.
   * :ballot_box_with_check: Se va descrie în documentație forma în care se apelează programul, plus 1-2 exemple de apel.

:ballot_box_with_check:(5%)
   * :ballot_box_with_check: Citirea din fisier
   * :ballot_box_with_check: Memorarea starii
   * :ballot_box_with_check: Parsarea fișierului de input care respectă formatul cerut în enunț

:ballot_box_with_check:(15%) Functia de generare a succesorilor

:ballot_box_with_check:(5%) Calcularea costului pentru o mutare

:ballot_box_with_check:(10%) Testarea ajungerii în starea scop (indicat ar fi printr-o funcție de testare a scopului)

:ballot_box_with_check:(2%) euristica banala

:ballot_box_with_check:(5%+5%) doua euristici admisibile posibile (se va justifica la prezentare si in documentație de ce sunt admisibile)

:ballot_box_with_check:(3%) o euristică neadmisibilă (se va da un exemplu prin care se demonstrează că nu e admisibilă).

   * Atenție, euristica neadmisibilă trebuie să depindă de stare (să se calculeze în funcție de valori care descriu starea pentru care e calculată euristica).

:ballot_box_with_check: (10%) crearea a 4 fisiere de input cu urmatoarele proprietati:

 :ballot_box_with_check: 1. un fisier de input care nu are solutii
 
 :ballot_box_with_check: 2. un fisier de input care da o stare initiala care este si finala (daca acest lucru NU e realizabil pentru problema, aleasa, veti mentiona acest lucru, explicand si motivul).
 
 :ballot_box_with_check: 3. un fisier de input care nu blochează pe niciun algoritm și să aibă ca soluții drumuri lungime micuță (ca să fie ușor de urmărit), să zicem de lungime maxim 20.
 
 :ballot_box_with_check: 4. un fisier de input care să blocheze un algoritm la timeout, dar minim un alt algoritm să dea soluție
 
 * dintre ultimele doua fisiere, cel putin un fisier sa dea drumul de cost minim pentru euristicile admisibile si un drum care nu e de cost minim pentru cea euristica neadmisibila

:ballot_box_with_check: (15%) Pentru cele NSOL drumuri(soluții) returnate de fiecare algoritm se va afișa:

 :x: 1. numărul de ordine al fiecărui nod din drum
 
 :ballot_box_with_check: 2. lungimea drumului
 
 :ballot_box_with_check: 3. costului drumului
 
 :ballot_box_with_check: 4. timpul de găsire a unei soluții (atenție, pentru soluțiile de la a doua încolo timpul se consideră tot de la începutul execuției algoritmului și nu de la ultima soluție)
 
 :ballot_box_with_check: 5. numărul maxim de noduri existente la un moment dat în memorie
 
 :ballot_box_with_check: 6. numărul total de noduri calculate (totalul de succesori generati; atenție la DFI și IDA* se adună pentru fiecare iteratie chiar dacă se repetă generarea arborelui, nodurile se vor contoriza de fiecare dată afișându-se totalul pe toate iterațiile
 
 :ballot_box_with_check: 7. între două soluții se va scrie un separator, sau soluțiile se vor scrie în fișiere diferite.
 
 * Obținerea soluțiilor se va face cu ajutorul fiecăruia dintre algoritmii studiați:
 
    * problema se va rula cu algoritmii: UCS, A* (varianta care dă toate drumurile), A* optimizat (cu listele open și closed, care dă doar drumul de cost minim), IDA*.
    
    * Pentru toate variantele de A* (cel care oferă toate drumurile, cel optimizat pentru o singură soluție, și IDA*) se va rezolva problema cu fiecare dintre euristici. Fiecare din algoritmi va fi rulat cu timeout, si se va opri daca depășește acel timeout (necesar în special pentru fișierul fără soluții unde ajunge să facă tot arborele).

:ballot_box_with_check: (5%) Afisarea in fisierele de output in formatul cerut

:ballot_box_with_check:(5%) Validări și optimizari. Veți implementa elementele de mai jos care se potrivesc cu varianta de temă alocată vouă:

 :ballot_box_with_check: 1. găsirea unui mod de reprezentare a stării, cât mai eficient
 
 :ballot_box_with_check: 2. verificarea corectitudinii datelor de intrare
 
 :ballot_box_with_check: 3. găsirea unor conditii din care sa reiasă că o stare nu are cum sa contina in subarborele de succesori o stare finala deci nu mai merita expandata (nu are cum să se ajungă prin starea respectivă la o stare scop)
 
 :ballot_box_with_check: 4. găsirea unui mod de a realiza din starea initială că problema nu are soluții.
 
  * Validările și optimizările se vor descrie pe scurt în documentație.

:ballot_box_with_check: (5%) Comentarii pentru clasele și funcțiile adăugate de voi în program . Comentariile pentru funcții trebuie să respecte un stil consacrat prin care se precizează tipul și rolurile parametrilor, căt și valoarea returnată (de exemplu, reStructured text sau Google python docstrings).

:ballot_box_with_check: (5%) Documentație cuprinzând explicarea euristicilor folosite. În cazul euristicilor admisibile, se va dovedi că sunt admisibile.

 :ballot_box_with_check: * În cazul euristicii neadmisibile, se va găsi un exemplu de stare dintr-un drum dat, pentru care h-ul estimat este mai mare decât h-ul real.
 
 :ballot_box_with_check: * Se va crea un tabel în documentație cuprinzând informațiile afișate pentru fiecare algoritm (lungimea și costul drumului, numărul maxim de noduri existente la un moment dat în memorie, numărul total de noduri).
 
 :ballot_box_with_check: * Pentru variantele de A* vor fi mai multe coloane în tabelul din documentație: câte o coloană pentru fiecare euristică.
 
 :ballot_box_with_check: * Tabelul va conține datele pentru minim 2 fișiere de input, printre care și fișierul de input care dă drum diferit pentru euristica neadmisibilă.
 
 :ballot_box_with_check: * În caz că nu se găsește cu euristica neadmisibilă un prim drum care să nu fie de cost minim, se acceptă și cazul în care cu euristica neadmisibilă se obțin drumurile în altă ordine decât crescătoare după cost, adică diferența să se vadă abia la drumul cu numărul K, K>1).
 
 :ballot_box_with_check: * Se va realiza sub tabel o comparație între algoritmi și soluțiile returnate, pe baza datelor din tabel, precizând și care algoritm e mai eficient în funcție de situație.
 
 :ballot_box_with_check: * Se vor indica pe baza tabelului ce dezavantaje are fiecare algoritm.


