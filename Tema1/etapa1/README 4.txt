	TODO2
	
Pentru a implementa această funcție în Racket, putem folosi o abordare recursivă pe coadă cu ajutorul funcției reverse. Primim lista preferințelor femeilor, wpref, și folosim o funcție auxiliară care va fi recursiv apelată pentru fiecare element din listă. În fiecare pas, se adaugă primul element din sublista curentă la rezultat și se continuă cu restul sublistei, până când sublista este goală.

În funcția get-women, apelăm funcția auxiliară get-women-helper cu lista preferințelor femeilor wpref și o listă goală acc pentru a stoca rezultatul. Funcția get-women-helper are două cazuri: dacă lista preferințelor femeilor este goală, atunci întoarce rezultatul inversat din acc, altfel adaugă prima sublistă la începutul listei acc și continuă recursiv cu restul listei preferințelor femeilor.
	
	TODO 3
	
Această implementare verifică dacă lista de preferințe este goală și, în caz afirmativ, întoarce o listă goală. În caz contrar, verifică dacă prima persoană din lista de preferințe este persoana dată, și, dacă da, întoarce lista de preferințe a acelei persoane. În caz contrar, se apelează recursiv funcția get-pref-list pe restul listei de preferințe.
	
	TODO 4

Această implementare utilizează operatorul cond pentru a verifica fiecare element din lista de preferințe.

Dacă primul element din listă este egal cu x, atunci x este preferat înaintea lui y și se întoarce true.

Dacă primul element din listă este egal cu y, atunci y este preferat înaintea lui x și se întoarce false.

În caz contrar, se continuă recursivitatea pe restul listei de preferințe, fără a fi nevoie să folosim operatori logici cum ar fi and sau or.

putând înlocui blocurile if cu expresii cond și folosind operatori logici pentru evaluarea condițiilor.

	TODO 5
The function takes a list of engagements (pairs of partners) and a person as arguments. It uses the cond expression to check three cases:

If the list of engagements is empty, return false.
If the first element of the first pair in the list of engagements is equal to the given person, return the second element of that pair (i.e., the partner).
If neither of the previous cases is true, recursively call the function with the rest of the engagements list.

	






