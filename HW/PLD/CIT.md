
CPLD
		- Je programovatelne
		- Spojeni vice obvodu GAL/PAL, ktere jsou vzajemne propojeny programovatelnymi propojvacimi poli
		-  Mohou nahradit nekolik tisic az stovky tisic logickych hradel
		- Programuji se pomoci vyhrazeneho rozhrani (napr JTAG)
		- Obrazek viz sesit.

Topologie FPGA obvodu
		- Dva zakladni typy FPGA podle ulozeni konfiguraci - volatilni a nevolatilni

Topologie s volatilni konfiguraci
		- SRA pametove bunky, lze menit konfiguraci za behu
	- Vyhody:
		- snadna konfigurace
	-Nevyhody:
		- Po startu systemu musi byt nakonfigurovan -> vetsi potrebny prostor na desce a cas pro konfiguraci

Topologie s nevolatilni konfiguraci
			- wda
		-Vyhody:
			- lepsi zabezpeceni
		- Nevyhody:
			- obtiznejsi zmena konfigurace

IOB a LB
	- vstupne-vystupni obvody pro kazdy v-v pin FPGA
	- obsahuji registr, budic, multiplexr a ochranne obvody
	- LB -> Logic Block predstavuji vlastni programovatelne logicke bloky
	- Vsechny bloky mohou byt propojeny globalni propojovaci matici

Dalsi soucasti

	- Blokove pameti - RAM, ROM
	- Aritmeticke obvody 
	- Bloky pro spravu a genetovani hodinovych signalu
- 