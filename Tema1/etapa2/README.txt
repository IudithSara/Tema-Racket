	TODO 2
O altă soluție ar fi să folosim funcția map pentru a transforma listele de preferințe ale bărbaților și femeilor în liste care conțin doar numele persoanelor (în loc de perechi de forma (nume . preferințe)), iar apoi să folosim funcția foldr pentru a adăuga numele bărbaților într-o listă goală. Codul ar arăta astfel:
În acest caz, nu mai este nevoie de operații de tip append sau reverse, deoarece lista rezultată este construită prin adăugarea elementelor în ordine inversă, fără a fi nevoie să se inverseze la final.

	TODO4
Am inlocuit testele eq? cu member, si pentru asta am definit o lista cu elementele x si y, si verificam daca primul element din pref-list este membru in aceasta lista.


	TODO5
Pentru a implementa această funcțională putem folosi o funcțională auxiliară care primește un acumulator acc și o listă L. Această funcțională va verifica dacă primul element din L satisface predicatul p și dacă da, va întoarce acest element, altfel va apela recursiv funcționala pe restul listei L.
În cazul în care lista este vidă, vom întoarce false.
Funcția find-first apelează funcția auxiliară find-first-helper cu un acumulator vid și lista dată ca argument. Funcția auxiliară va explora lista până când găsește primul element care satisface predicatul p, moment în care va întoarce acest element. Dacă nu există astfel de elemente în lista, funcția auxiliară va întoarce false.

	TODO6
În această variantă, folosim o funcție anonimă match-pair? pentru a verifica dacă primul element al unui cuplu din listă este egal cu person. Apoi, folosim funcționala find-first pentru a căuta primul cuplu din listă care satisface acest predicat. Dacă găsim un astfel de cuplu, întoarcem al doilea său element (partenerul lui person), altfel întoarcem #f. De asemenea, am eliminat cazul null? engagements din cond și l-am înlocuit cu un let care ne permite să definim valoarea lui match doar o dată și să o folosim în continuare în condiția din if.

	TODO7
This implementation recursively traverses the list L, checking each element against the predicate p. When the first element is found that satisfies p, it's replaced with the new value val using the cons function. The remaining elements are left untouched. If no element in the list satisfies p, the original list is returned unchanged.

	TODO8
Una dintre abordările posibile pentru implementarea funcției update-engagements este să parcugem lista engagements, căutând perechea cu prima componentă egală cu p1. Apoi, cu ajutorul funcției change-first, vom înlocui vechiul partener al lui p1 cu p2.
Funcția începe prin a salva în variabila old-partner vechiul partener al lui p1. Aceasta este valoarea întoarsă de funcția get-partner, sau #f dacă p1 nu era logodită anterior.
Apoi, dacă p1 era logodită anterior, funcția folosește change-first pentru a înlocui vechiul partener al lui p1 cu p2. Mai exact, predicatul dat ca prim argument lui change-first caută prima pereche care are al doilea component old-partner, și o înlocuiește cu o nouă pereche ce conține p1 și p2. Dacă p1 nu era logodită anterior, lista originală engagements este întoarsă fără modificări.
Notă: Funcția get-partner trebuie implementată în prealabil, așa cum s-a făcut mai sus.
	
	TODO9
	
