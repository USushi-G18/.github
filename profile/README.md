# Progetto Team-18 (Ingegneria del Software - A.A. 2023/2024)
Organizzazione del progetto U-Sushi, una webapp sviluppata per il corso di Ingegneria del Software a.a 2023/2024 dell'Università degli Studi di Trento.
In questa organizzazione si trovano 3 repository:
 - Frontend (sviluppato in Svelte) per la parte grafica
 - Backend (sviluppato in Go) per lo sviluppo di API
 - Deliverables per la consegna dei documenti di progettazione

Team: [Di Cesare Daniele](https://github.com/DiCesareDaniele) (Team Leader), [Tonini Isaia](https://github.com/Isax03), [Zendri Matteo](https://github.com/ZendriXXX)

# Screenshots

## hosomaki
![screenshot](images/hosomaki.png)

## piatti
![screenshot](images/plates.png)

## login
![screenshot](images/login.png)

## cucina
![screenshot](images/kitchen.png)

## carrello 
![screenshot](images/cart.png)

## categorie 
![screenshot](images/categories.png)

# Eseguire in locale 
- Frontend:
Per prima cosa è necessario clonare la repo GitHub del frontend tramite il link
https://github.com/USushi-G18/frontend.git.
A clonazione terminata eseguire (dentro alla directory) il comando npm install
--force per installare le dipendenze necessarie.
NOTA: l’opzione force si rende necessaria a causa di un warning dato da
svelte-navigator in relazione con Vite
Al termine dell’installazione delle dipendenze, eseguire il comando npm run dev
Il sito si può visitare all’url http://localhost:5173 (può variare la porta, seguire le
istruzioni sul terminale).
- Backend:
Per il backend è necessario avere Docker installato. Soddisfatto questo requisito è
necessario clonare la repository tramite il link
https://github.com/USushi-G18/backend.git. È necessario poi generare una chiave
pem e per farlo basta creare una cartella /secrets nella root del progetto ed
eseguire il seguente comando nella cartella appena creata:
openssl genrsa -out key.pem 2048.
Generata la chiave, basta eseguire (all’interno della cartella principale del progetto) il
comando docker compose up -d --build.
Le APIs esposte dal backend si possono raggiungere sul localhost e sulle porte 8081
per l’admin e 8082 per i clienti e la cucina: 
admin -> http://localhost:8081/admin, clienti -> http://localhost:8082/client, cucina -> http://localhost:8082/employee
