# I/O and HDD/SSD

- Ranger disse metodene for I/O i hanhold til CPU bruk. DVS minst bruk/involvering av CPU bør være nr 1 og mest brukt/involvering av CPU bør være nr 3.
	1. DMA. 
	2. Interupt I/O.
	3. Programmet.


- For at CPU skal kunne kommuniserer med I/O enheter 
	  1.  Fysisk minne
	  2. I/O-Porter

- Oprativsystemkjernen må håndtere I/O-enheter generelt, så hvilke deler av oprativsystemet har kode for å prate detaljert med hver type I/O enhet
	- Driverer/moduler.

- Er du enig i disse påstandende im HDD
	- HDD har en mekanisk bevegelig arm for hver plateoverflate
	- (Aksesstiden for å lese/skrive data på en HDD er primært bestemt av tiden det tar å lese/skrive på platen.)

- HDD med 10000 RPM og søketid (avrage seektime) 4mn, hvor lang tid det gjennomsnittlig for å lese / skrive-armen å komme til dataene?
	- 0,006 for en runde aka 6MS = 7 ms = 4ms+3ms

- 