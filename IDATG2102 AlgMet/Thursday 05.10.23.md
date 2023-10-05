- [[#Egenskaper for 2-3-4 trær|Egenskaper for 2-3-4 trær]]
- [[#Noen egenskaper for Red-Black trær|Noen egenskaper for Red-Black trær]]
# Balanserte trær
- Dette sammendraget handler om betydningen av å opprettholde **balanse i trær**, spesielt i forbindelse med operasjoner som **insert, remove/delete** og **search** for å maksimere effektiviteten. Balanserte trær er de hvor forskjellen i dybde mellom noder på det laveste nivået og de på det høyeste nivået er begrenset. Grad av tillatt forskjell avgjør hvor balansert treet er.

Det nevnes flere algoritmer og metoder for å oppnå balanserte trær, inkludert **2-3-4 trær, Red-Black trær, AVL trær, Splay trær, AA trær, Scapegoat trær og Treap**. Teksten fokuserer på de to første algoritmene, 2-3-4 trær og Red-Black trær, som sikrer at noder på høyeste nivå er maksimalt dobbelt så dypt som de på laveste nivå.

Selv om disse algoritmene kan virke komplekse i koden, fokuserer teksten på prinsippene bak deres funksjon i stedet for å gå inn i detaljert kode. Det antydes at det er enkelt å finne kodeeksempler for begge algoritmene ved å utføre Google-søk.

#### Egenskaper for 2-3-4 trær
- Søk trenger aldri å besøke mer en lg N +1 noder.
- *innstting* krever i *værste fall* færre enn N + 1 nodesplitter, og later gjennomsnitlig ut til å kreve mindre enn en *splitting*

#### Noen egenskaper for Red-Black trær
- Det er *aldri* to Red-linker rett etter hverandre på enhver sti til rota og ned til bladnode (ingen node kan være del av mor, og mor en del av bestemor også.)
- Alle stier har det samme antall black-linkerø. (Det ser vi enklest av det tilsvarende 2-3-4 treet, der alle bladnoder slutter likt, dvs. samme antall Black ned til dem.)
- **Sti med annenhver gang Red- og Black link kan max. være dobbelt så lang som
	en sti med kun Black.** (Derfor er høyeste nivå max. det dobbelte av laveste.)
- **Verdier/keyer kan, pga. splitting, havne på begge sider av en lik key!**
	(Derfor må en evt. ‘search’-funksjon håndtere dette også.)