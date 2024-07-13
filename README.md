scrivi una applicazione web Spring Boot con le seguenti librerie:
Lombok
Spring Boot DevTools
Spring Web
Spring Data JPA
MySQL Driver
usa hibernate e JPA per connettersi alla base dati mysql locale (e.g. devdb)
configura il parametro ddl-auto così che hibernate crea e distrugge lo schema alla fine della sessione
considera questo use case:
1 student ---> n enrollments
1 class ---> n enrollments
avendo in mente gli usecase di cui sopra e usando le annotazioni, scrivi il codice per creare:
la tabella students dove ogni studente avrà:
primary key
colonna lastName (not null)
colonna firstName (not null)
colonna email con valori univoci e not null
la tabella classes dove ogni classe ha:
primary key
title (not null)
description (not null)
tabella enrollments per salvare collegamenti tra le tabelle students e classes:
primary key
2 foreign keys
