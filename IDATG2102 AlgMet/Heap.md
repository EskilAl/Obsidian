# En heap
- ligner noe på stakk/kø
- er grei å bruke når stadig skal operere på det største/minste elementet.
- *er en array ordnet etter visse (heap)betingelser*.
- Poenget: Delvis sortert, raskt å få tak i det neste og største(minste) elementet.

# Prinsippene er en heap (hvordan man bygger/lager/vedlikeholder den):
1. Dersom alle verdiene legges inn i et binært tre, så skal treet tilfredstille **heap-betingelsen**: *Enhver nodes verdi/key/ID er større (eller lik) verdien i barna* (om den har noen). Dette medfører at den største verdien til enhver tid er/ligger i treets rot.
2. Treet som bygges er et komplett tre
3. Vi traverserer/leser dette treet *level order , og legger verdiene fortløpende inn i en array.* Dermed har vi fått en array som tilfredstiller heap-betingelsen! Og den største verdien ligger først i arrayen (med indeks nr.1 I element nr.0 (null) ligger det stort sett en *sentinel key*).
4. Foreldre/mora til element nr .j, ligger i element nr j/2 (oddetall avrundes nedover). Og evt. barnene til element nr i, ligger i element nr . i*2 og (i*2)+1.