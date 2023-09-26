## Scheduling
Cpu-tidsbruk(viktig å se sammenheng med scheduling policy, og mekanismene bi lærte om i forrige tema.)
En regnekrevende process bruker 2 minutter på en cpu med hyoerthreading, hvor lang tid bruker seks slike prosesorer på en quad-core cpu uten hyperthreading(quad-core = fire CPU'er).

- 3minutter = (6 * 2/4)=3

Hva blir gjennomsnittlig turnaround-tid for ./schedluer.py -p FIFI -l 5, 5, 5, 5
(samme ankmsttid for alle fire prosessene)

- (5 + 10 + 15 + 20)/4 = 12,5

Når funker FIFO/FCFS dårlig (mtp turnaround-tid)?

- Hvis det er en stor prosses først i køen.

"Convoy-effekt"-problemet fil FIFO/FCFS løser hvis vi istedet benytter:

- Shortest job first

En preemptive versjon av SJF kalles

- shortest time-to completion first.

Hva blir gjennomsnittlig response-tid for RR - q 2 .l 5, 5, 5, 5 (Samme ankomsttid for alle fire prosessene, tidskavntum (q) er 2).

- (0 + 2 + 4 +6)/4 = 3

Vi bør brukt så korte tidskvantum som mulig bed Round-Robin scheduling siden det fordeler tiden mest rettferdig til alle prosessene. Enig? begrunn.

- Nei, Context switch tar tid. 

When a job enters the system, it is placed at the highest priority (the topmost queue)." Den er OK, men hvilke regler for å endre prioritetet?"






