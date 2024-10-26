<template>
  <header>
    <h1>Progetti da implementare</h1>
  </header>
  <main>
    <div class="card">
      <h2>Lista della Spesa Interattiva</h2>
      <ul>
        <li>Aggiungere prodotti</li>
        <li>Specificare la quantità</li>
        <li>Segnare quali prodotti sono già nel carrello</li>
        <li>Calcolare il totale stimato</li>
        <li>Possibilità di categorizzare i prodotti (frutta, verdura, ecc.)</li>
      </ul>
    </div>
    <div class="card">
      <h2>Gestione Appuntamenti</h2>
      <ul>
        <li>Inserisci nuovi appuntamenti con data e ora</li>
        <li>Visualizzi gli appuntamenti del giorno</li>
        <li>Puoi modificare o cancellare appuntamenti</li>
        <li>Ricevi un avviso per appuntamenti sovrapposti</li>
        <li>Categorizza gli appuntamenti (lavoro, personale, etc.)</li>
      </ul>
    </div>
    <div class="card">
      <h2>Calcolatrice del Budget</h2>
      <ul>
        <li>Inserisci entrate e uscite</li>
        <li>Categorizzi le spese</li>
        <li>Visualizzi un riepilogo mensile</li>
        <li>Crei obiettivi di risparmio</li>
        <li>Vedi statistiche delle tue spese</li>
      </ul>
    </div>
    <div class="card">
      <h2>Gestore di Ricette</h2>
      <ul>
        <li>Aggiungi nuove ricette</li>
        <li>Lista degli ingredienti necessari</li>
        <li>Tempo di preparazione</li>
        <li>Difficoltà</li>
        <li>Possibilità di cercare ricette per ingrediente</li>
        <li>Rating personale delle ricette provate</li>
      </ul>
    </div>
    <div class="card">
      <h2>Sistema di Votazione</h2>
      <ul>
        <li>Crei sondaggi</li>
        <li>Aggiungi opzioni di voto</li>
        <li>Visualizzi i risultati in tempo reale</li>
        <li>Mostri grafici dei risultati</li>
        <li>Permetti commenti sui sondaggi</li>
      </ul>
    </div>
    <div class="card">
      <h2>Tracker di Allenamento</h2>
      <ul>
        <li>Registrare gli esercizi svolti</li>
        <li>Tenere traccia dei progressi</li>
        <li>Impostare obiettivi</li>
        <li>Visualizzare statistiche</li>
        <li>Programmare allenamenti futuri</li>
      </ul>
    </div>
    <div class="card">
      <h2>Gestore di Libreria Personale</h2>
      <ul>
        <li>Catalogare i tuoi libri</li>
        <li>Segnare quelli letti/da leggere</li>
        <li>Dare valutazioni</li>
        <li>Aggiungere note e recensioni</li>
        <li>Organizzare per genere o autore</li>
      </ul>
    </div>
    <div class="card">
      <h2>Dashboard Meteo</h2>
      <ul>
        <li>Visualizzare il meteo attuale</li>
        <li>Previsioni per i prossimi giorni</li>
        <li>Salvare città preferite</li>
        <li>Mostrare dettagli come umidità, vento, etc.</li>
        <li>Avvisi per condizioni meteorologiche particolari</li>
      </ul>
    </div>
    <div class="card">
      <h2>Gestore di Note</h2>
      <ul>
        <li>Creare note testuali</li>
        <li>Organizzarle in categorie</li>
        <li>Cercare tra le note</li>
        <li>Aggiungere tag</li>
        <li>Impostare promemoria</li>
      </ul>
    </div>
    <div class="card">
      <h2>Quiz Interattivo</h2>
      <ul>
        <li>Crei domande e risposte</li>
        <li>Tieni traccia del punteggio</li>
        <li>Timer per le risposte</li>
        <li>Diverse categorie di domande</li>
        <li>Statistiche delle performance</li>
      </ul>
    </div>
  </main>
  <footer>
    <ListaDellaSpesa />
  </footer>
</template>

<script>

import ListaDellaSpesa from './components/ListaDellaSpesa.vue';

export default {
  components: {
    ListaDellaSpesa
  },
};

</script>

<style lang="css" scoped>
header,
main {
  margin: 10px;
}

h1 {
  text-align: center;
}

ul {
  list-style: none;
}
</style>