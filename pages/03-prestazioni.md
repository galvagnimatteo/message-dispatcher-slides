<SectionLabel label="Svantaggi" />

<div class="eyebrow">Carte in tavola</div>

# Due svantaggi, <em>gestibili</em>

<div class="grid grid-cols-2 gap-6 mt-4">
  <div class="card-amber">
    <div class="head-teal" style="color:var(--amber)">1 · Supporto legacy</div>
    <div class="text-sm" style="color:var(--ink-mid)">Non sarà possibile supportare le vecchie API: un frontend vecchio non potrà funzionare con un backend nuovo.</div>
    <div class="text-sm mt-2" style="color:var(--ink-mid)">L'opposto è invece supportato, dunque l'upgrade dovrà seguire l'ordine: prima frontend, poi backend.</div>
    <div class="text-sm mt-2" style="color:var(--ink-mid)"><strong>Da decidere:</strong> coordinamento con il rilascio della nuova app.</div>
  </div>
  <div class="card-amber">
    <div class="head-teal" style="color:var(--amber)">2 · Throughput su singola istanza</div>
    <div class="text-sm" style="color:var(--ink-mid)">Su una sola istanza è prevista una leggera diminuzione del throughput rispetto a MongooseIM.</div>
    <div class="text-sm mt-2" style="color:var(--ink-mid)">Tuttavia scala linearmente in multi-istanza, nativamente.</div>
  </div>
</div>

---

<SectionLabel label="Prestazioni" />

<div class="eyebrow">Lo abbiamo verificato</div>

# Comparazione delle <em>prestazioni</em>

<div class="grid grid-cols-3 gap-4 mt-4">
  <div class="card text-center">
    <div class="card-num">Throughput*</div>
    <div class="text-sm mt-1"><span style="color:var(--teal-dark);font-weight:700">MongooseIM</span> · 250-300 msg/s</div>
    <div class="text-sm mt-1"><span style="color:var(--teal-dark);font-weight:700">WSC</span> · 200-250 msg/s</div>
  </div>
  <div class="card text-center">
    <div class="card-num">Timeline</div>
    <div class="text-sm mt-1"><span style="color:var(--teal-dark);font-weight:700">MongooseIM</span> · ~200 ms</div>
    <div class="text-sm mt-1"><span style="color:var(--teal-dark);font-weight:700">WSC</span> · ~35 ms</div>
  </div>
  <div class="card text-center">
    <div class="card-num">Ricerca</div>
    <div class="text-sm mt-1"><span style="color:var(--teal-dark);font-weight:700">MongooseIM</span> · ~130 ms</div>
    <div class="text-sm mt-1"><span style="color:var(--teal-dark);font-weight:700">WSC</span> · ~37 ms</div>
  </div>
</div>

<div class="card-teal card-accent mt-4">
  <div class="head-teal">Il punto</div>
  <div class="text-sm" style="color:var(--ink-mid)">Scalabilità orizzontale, ricerca e cronologia veloci: <strong>tutto nativo e immediato</strong>, senza installare strumenti aggiuntivi. MongooseIM richiederebbe componenti extra (es. <strong>Elasticsearch</strong> per la ricerca) e configurazione dedicata per il multi-istanza.</div>
</div>
