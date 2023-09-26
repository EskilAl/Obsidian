# Permutering
Velkommen til en forklaring av algoritmen for permutering i EKS_19_Permutering.cpp/java! Her vil du lære hvordan du kan bytte rundt på alle elementene i en array på alle tenkelige måter ved hjelp av to hjelpefunksjoner og en rekursiv funksjon. Eksempel spørsmål:  
- Hva er forskjellen mellom venstrerotering og høyrerotering?  
- Kan denne algoritmen brukes på andre datastrukturer enn arrays?  
- Hvordan kan man optimalisere denne algoritmen for store arrays?

### Spørsmål
1. Spørsmål: **Hvordan kan jeg bruke denne algoritmen til å permutere en array med tall?**
	Svar: Du kan bruke funksjonen permuter(arr, i, n) til å generere alle permutasjoner av tallene i arrayen arr mellom indeksene i og n. For eksempel, hvis du har en array med tallene [1, 2, 3], kan du kalle funksjonen permuter(arr, 0, 2) for å generere alle mulige permutasjoner av tallene i arrayen mellom indeks 0 og 2.

2. Spørsmål: **Hva skjer når funksjonen permuter(arr, i, n) kalles?**
 Svar: Når funksjonen permuter(arr, i, n) kalles, genererer den alle permutasjoner av de elementene som i kalløyeblikket er i arr mellom indeksene i og n. Dette gjøres ved å flytte alle etterfølgende elementer etter nr. i ned i posisjon nr. i (vha. bytt(...)). For hver gang kaller den seg selv rekursivt slik at dette også gjøres for indeks i+1. Når denne parameteren har blitt n, er det ikke flere elementer igjen å permutere, og vi kan bruke/skrive ut arr.

3. Spørsmål: **Hvordan kan jeg venstrerotere en array med tall?**
	Svar: Du kan bruke funksjonen roterVenstre(arr, i, n) til å venstrerotere ett hakk innholdet i arr mellom indeksene i og n. For eksempel, hvis du har en array med tallene [1, 2, 3, 4, 5], kan du kalle funksjonen roterVenstre(arr, 2, 4) for å venstrerotere tallene mellom indeks 2 og 4, slik at arrayen blir [1, 2, 4, 3, 5].

|     | permuter(array,0,3)                               |    permuter(array,1,3)                                 |    permuter(array,2,3)  |
| --- | ------------------------------------------------- | --------------------------------------------------- | -------------------- |
| 1   | permuter(array,1,3)1<font color="red"> 2 3</font> |                                                     |                      |
| 2   |                                                   | permuter(array,2,3)1 2<font color="red"> 3</font>   |                      |
| 3   |                                                   |                                                     | display(array) 1 2 3 |
| 4   |                                                   | bytt(arr[1], arr[2]) 1 <font color="red">3 2</font> |                      |
| 5   |                                                   | permuter(array,2,3)1 3<font color="red"> 2</font>                                                    |                      |
| 6   |                                                   |                                                     | display(array) 1 3 2                      |
| 7   |                                                   |roterVenstre(array, 1, 3) 1 <font color="red">2 3</font>                                                     |                      |
| 8   | bytt(arr[0], arr[1])<font color="red">2 1</font> 3                                                  |                                                     |                      |
| 9   |permuter(array,1,3)2<font color="red"> 1 3</font>                                                   |                                                     |                      |
| 10  |                                                   |permuter(array,2,3)2 1<font color="red"> 3</font>                                                     |                      |
| 11  |                                                   |                                                     |display(array) 2 1 3                    |
| 12  |                                                   |bytt(arr[1], arr[2]) 2 <font color="red">3 1</font>                                                     |                      |
| 13  |                                                   |permuter(array,2,3)2 3<font color="red"> 1</font>                                                     |                      |
| 14  |                                                   |                                                     |display(array) 2 3 1                      |
| 15  |                                                   |roterVenstre(array, 1, 3) 2 <font color="red">1 3</font>                                                     |                      |
| 16  |bytt(arr[0], arr[2])<font color="red">3</font> 1 <font color="red">2</font>                                                   |                                                     |                      |
| 17  |permuter(array,1,3)3<font color="red"> 1 2</font>                                                   |                                                     |                      |
| 18  |                                                   |permuter(array,2,3)3 1<font color="red"> 2</font>                                                     |                      |
| 19  |                                                   |                                                     |display(array) 3 1 2                      |
| 20  |                                                   |bytt(arr[1], arr[2]) 3 <font color="red">2 1</font>                                                     |                      |
| 21  |                                                   |permuter(array,2,3)3 2<font color="red"> 1</font>                                                     |                      |
| 22  |                                                   |                                                     |display(array) 3 2 1                      |
| 23  |                                                   |roterVenstre(array, 1, 3)3 <font color="red">1 2</font>                                                     |                      |
| 24  |roterVenstre(array, 0, 3)<font color="red">1 2 3</font>                                                   |                                                     |                      |
