# En heap
- ligner noe på stakk/kø
- er grei å bruke når stadig skal operere på det største/minste elementet.
- *er en array ordnet etter visse (heap)betingelser*.
- Poenget: Delvis sortert, raskt å få tak i det neste og største(minste) elementet.

# Prinsippene er en heap (hvordan man bygger/lager/vedlikeholder den):
1. Dersom alle verdiene legges inn i et binært tre, så skal treet tilfredstille **heap-betingelsen**: *Enhver nodes verdi/key/ID er større (eller lik) verdien i barna* (om den har noen). Dette medfører at den største verdien til enhver tid er/ligger i treets rot.
2. Treet som bygges er et komplett tre
3. Vi traverserer/leser dette