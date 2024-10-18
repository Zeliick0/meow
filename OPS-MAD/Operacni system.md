
- Sklada se z: 1. Kernelu, 2. Prikazoveho radku, 3.Graficke rozhrani ( Uzivatelske rozhrani), 4. Drivery, 5. Aplikace 3. stran 
	
- OS Zajistuje spravu: Procesu, Pameti, Souboroveho systemu, Periferii, Uzivatelskeho rozhrani


#### ==OS - Absatrakce==
- ==Proces==
  - Cinnost kterou ridi program
   - Zakodovany navod na prislusnou cinnost

- ==Soubor==
	- Kolekce zaznamu
	- Zakladni jednotka pro ukladani dat

- ==Adresar==
	- Kolekce souboru
	- Specialny typ souboru -> adresarovy soubor


#### ==Jadro==
- Core, kernel
￼￼- Nejnizsi a nejzakladneji cast OS

- Zavadeno jako prvni pri staru OS
	- Bezi po celou jeho dobu

- ==Kontrola nad PC==
	- Bezi v privilegovanem rezimu
	- Nutna podpora v CPU
	- Libovolne operace nad HW
	- Prepinani kontextu (procesy)
	- Prace s virtualni pameti (strankovani, segmentace)
	- Nastavovani parametru HW

- ==Systemove volani==
	- vyuziva system nebo uzivatelske programy pro sluzby jadra
	- Speacialni instrukce OS
	- Kontrolovany prechod do rezimu jadra

- ==Volani jadra==
	1. ==Kernel interface==
		- Prime volani pomoci speacialni instrukce
		- HLT | ADD A, #2 | MOV 0x23 , @R0
	2. ==Library interface== 
		- Vyuziti systemovych knihoven
		- Nemusi vest k volani sluzeb jadra
		- fopen() | fwrite()

- ==Sluzby jadra dostupne v UNIXu==

	- ==Open/close==
		-  otevreni/zavreni souboru
	- ==read/write==
		- Cteni/zapis souboru
	- ==kill [ PID]==
		- signal pro ukonceni procesu
	- ==fork==
		- vytvoreni potomka - duplikace procesu
	- ==exec==
		- vykonani prikazu v prikazu (prepsani kodu)
	- ==exit==
		- ukonceni procesu

- ==Typy jader==
	- ==Monoliticke
		- a) Nemodularni 
			- MS-DOS, WIN95, MAC OS (do verze 8.6)
		- b) Modularni
			- Linux, NetBSD, OpenBSD...
	- ==Mikrojadro==
		- Minix, Symbian OS
	- ==Hybridni==
		- Vetsina soucasnych OS
		- MACOS X, WIN XP nahoru
	- ==Exo==
		- Aexis, Nemesis
	- ==Nano==


### ==Monoliticke jadro
![[Pasted image 20240927122010.png]]

- ==Komplexni jadro
	- Bezi v privilegovanem rezimu 
		- Vsechny subsystemy implementujici sluzby jsou tesne provazany -> vysoka efektivita
		- Sprava pameti, planovani, meziprocesni komunikace, souborove systemy, podpora sitove komunikace

- Chyba v jednom subsystemu muze ovlivnit dalsi, pripadne az shodit cele jadro
	- Sdili stejny adresni prostor

- ==Dynamicke nahravani modulu==
	- Vylepseni koncepce
	- Moznost nahrani za behu systemu bez nutnosti restartu
		- USB flash
		- Sitovy protokol
	- Zavedeny do adresniho prostoru jadra
	- Jiste zpozdeni
		- Nahravany pri startu systemu
	- 