# Changelog

Tutte le modifiche rilevanti a questo plugin sono documentate in questo file.

Il formato è basato su [Keep a Changelog](https://keepachangelog.com/it/1.1.0/)
e questo progetto aderisce al [Semantic Versioning](https://semver.org/lang/it/).

## [1.0.1] - 2026-11-03

### Fixed
- Temi a blocchi: l'avviso compariva due volte sotto il prezzo nella scheda prodotto (una dal hook della scheda e una dal
  blocco «Prezzo prodotto»). Ora compare una sola volta.

## [1.0.0] - 2026-11-03

### Added
- Storico prezzi per prodotto semplice e per variazione: ogni variazione del prezzo effettivo viene registrata
  (salvataggio da admin, modifica rapida/di massa, REST API, importazioni via CRUD WooCommerce, sconti programmati).
- Allineamento giornaliero in cron per i cambi di prezzo che non passano dal CRUD (importazioni SQL, altri plugin) e
  pulizia dello storico oltre la retention.
- Prezzo di riferimento Omnibus: il più basso dei N giorni (30 per legge) precedenti all'applicazione dello sconto;
  con riduzioni successive resta quello precedente alla prima riduzione.
- Avviso "Prezzo più basso negli ultimi {days} giorni prima dello sconto: {price}" in scheda prodotto, elenchi
  prodotti e carrello classico, anche nei temi a blocchi (blocco Prezzo prodotto). Testo configurabile.
- Prodotti variabili: avviso sulla variazione scelta; sul prodotto genitore (intervallo min–max) solo se tutte le
  variazioni ne hanno diritto.
- Pagina impostazioni in WooCommerce → Omnibus: attivazione (spenta di default), giorni, dove mostrare, solo in
  offerta, testo, retention, cancellazione dati alla disinstallazione.
- Prezzo di riferimento mostrato con le tasse come il prezzo del negozio (inclusive/esclusive).
- Compatibilità dichiarata con HPOS e checkout a blocchi. Traduzione it_IT.
