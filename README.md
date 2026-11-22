<!doctype html>
<html lang="en" data-theme="system">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>WANE: Ways Around Neuroscience Efficiently</title>
<style>
:root{
  --bg:#f6f8fb; --surface:#ffffff; --text:#14202e; --muted:#4a5a6c;
  --accent:#1f6feb; --accent-text:#ffffff; --border:#d5dde7; --warn:#8a5a00; --warn-bg:#fff4d6;
}
@media (prefers-color-scheme: dark){
  :root[data-theme="system"]{
    --bg:#0c1320; --surface:#152032; --text:#e8eef6; --muted:#a9b7c8;
    --accent:#6cb2ff; --accent-text:#0c1320; --border:#2a3a52; --warn:#ffd77a; --warn-bg:#3a2e10;
  }
}
:root[data-theme="dark"]{
  --bg:#0c1320; --surface:#152032; --text:#e8eef6; --muted:#a9b7c8;
  --accent:#6cb2ff; --accent-text:#0c1320; --border:#2a3a52; --warn:#ffd77a; --warn-bg:#3a2e10;
}
:root[data-theme="light"]{
  --bg:#f6f8fb; --surface:#ffffff; --text:#14202e; --muted:#4a5a6c;
  --accent:#1f6feb; --accent-text:#ffffff; --border:#d5dde7; --warn:#8a5a00; --warn-bg:#fff4d6;
}
*{box-sizing:border-box}
body{margin:0;font-family:system-ui,-apple-system,"Segoe UI",Roboto,sans-serif;background:var(--bg);color:var(--text);line-height:1.6}
a{color:var(--accent)}
header,main,footer{max-width:1000px;margin:0 auto;padding:0 1rem}
header{display:flex;flex-wrap:wrap;justify-content:space-between;align-items:center;gap:.75rem;padding-top:1rem}
.brand h1{margin:0;font-size:1.4rem}
.brand p{margin:0;color:var(--muted);font-size:.9rem}
nav a{margin-left:1rem;text-decoration:none;font-weight:600}
button,select,input,textarea{font:inherit}
button{background:var(--accent);color:var(--accent-text);border:0;border-radius:8px;padding:.5rem .9rem;cursor:pointer}
button.secondary{background:transparent;color:var(--text);border:1px solid var(--border)}
button:focus-visible,input:focus-visible,select:focus-visible,textarea:focus-visible,a:focus-visible{outline:3px solid var(--accent);outline-offset:2px}
input,select,textarea{background:var(--surface);color:var(--text);border:1px solid var(--border);border-radius:8px;padding:.5rem .7rem;width:100%}
.hero{background:var(--surface);border:1px solid var(--border);border-radius:14px;padding:1.5rem;margin-top:1.25rem}
.hero h2{margin:.2rem 0;font-size:1.8rem}
.tagline{color:var(--accent);font-weight:600;margin:0}
.levels{display:flex;flex-wrap:wrap;gap:.5rem;margin:1rem 0}
.levels button.active{outline:3px solid var(--accent);outline-offset:1px}
.search-row{display:grid;grid-template-columns:2fr 1fr 1fr 1fr;gap:.5rem;margin-top:1rem}
@media (max-width:700px){.search-row{grid-template-columns:1fr}}
section{margin-top:1.5rem}
h3{margin-bottom:.4rem}
.grid{display:grid;grid-template-columns:repeat(auto-fill,minmax(260px,1fr));gap:.9rem}
.card{background:var(--surface);border:1px solid var(--border);border-radius:12px;padding:1rem;cursor:pointer;text-align:left}
.card h4{margin:.2rem 0;font-size:1.05rem}
.meta{color:var(--muted);font-size:.85rem}
.badge{display:inline-block;font-size:.75rem;border:1px solid var(--border);border-radius:999px;padding:.05rem .5rem;margin-right:.3rem;color:var(--muted)}
.draft{background:var(--warn-bg);color:var(--warn);border-radius:6px;padding:.25rem .5rem;font-size:.85rem;display:inline-block;margin:.4rem 0}
.disclaimer{background:var(--warn-bg);color:var(--warn);border-radius:10px;padding:.75rem 1rem;margin:1rem 0;font-size:.92rem}
.hidden{display:none!important}
#detail{background:var(--surface);border:1px solid var(--border);border-radius:14px;padding:1.5rem;margin-top:1.25rem}
#detail ul{padding-left:1.2rem}
.panel{background:var(--surface);border:1px solid var(--border);border-radius:14px;padding:1.25rem;margin-top:1.25rem}
.row{display:flex;gap:.5rem;flex-wrap:wrap;align-items:center}
.card-item{border:1px solid var(--border);border-radius:10px;padding:.75rem;margin-top:.6rem;background:var(--bg)}
.card-item p{margin:.2rem 0}
footer{margin-top:3rem;padding-bottom:2rem;color:var(--muted);font-size:.85rem;border-top:1px solid var(--border);padding-top:1rem}
.empty{color:var(--muted)}
.skip{position:absolute;left:-9999px}
.skip:focus{left:1rem;top:1rem;background:var(--surface);padding:.5rem;z-index:10}
</style>
</head>
<body>
<a class="skip" href="#main">Skip to content</a>

<header>
  <div class="brand">
    <h1>WANE</h1>
    <p>Ways Around Neuroscience Efficiently</p>
  </div>
  <nav aria-label="Primary">
    <a href="#" data-view="home">Home</a>
    <a href="#" data-view="study">Study</a>
    <a href="#" data-view="about">About</a>
    <a href="#" data-view="legal">Legal</a>
  </nav>
  <div class="row">
    <label for="themeSel" class="meta">Theme</label>
    <select id="themeSel" style="width:auto">
      <option value="system">System</option>
      <option value="light">Light</option>
      <option value="dark">Dark</option>
    </select>
  </div>
</header>

<main id="main">

<!-- HOME -->
<div id="view-home">
  <div class="hero">
    <p class="tagline">Explore the brain. Learn at your level.</p>
    <h2>Neuroscience and neurosurgery, explained step by step</h2>
    <p>WANE is a searchable, filterable library of topics, terms, and procedures for beginners and advanced learners. Pick your level, then search or browse.</p>
    <div class="disclaimer" role="note">
      WANE is an educational resource. It is not a substitute for a qualified clinician, medical training, or professional advice. Do not use it to diagnose or treat any condition.
    </div>

    <h3>Choose your level</h3>
    <div class="levels" role="group" aria-label="Learning level">
      <button class="secondary" data-level="Curious">Curious</button>
      <button class="secondary" data-level="High School">High School</button>
      <button class="secondary" data-level="Premed">Premed</button>
      <button class="secondary" data-level="Med School">Med School</button>
      <button class="secondary" data-level="Researcher">Researcher</button>
      <button class="secondary" data-level="Lecturer">Lecturer</button>
    </div>
    <p class="meta" id="levelNote">No level selected. Showing all content. You can change your level at any time.</p>

    <form id="searchForm" role="search">
      <label for="q" class="meta">Search topics and resources</label>
      <div class="search-row">
        <input id="q" type="search" placeholder="e.g. synapse, Broca, blood-brain barrier">
        <select id="fType" aria-label="Filter by content type">
          <option value="">All types</option>
          <option>Topic</option>
          <option>Procedure</option>
          <option>Terminology</option>
          <option>Imaging</option>
        </select>
        <select id="fLevel" aria-label="Filter by learning level">
          <option value="">All levels</option>
          <option>Curious</option><option>High School</option><option>Premed</option>
          <option>Med School</option><option>Researcher</option><option>Lecturer</option>
        </select>
        <select id="fDate" aria-label="Filter by date">
          <option value="">Any date</option>
          <option value="newest">Newest first</option>
          <option value="oldest">Oldest first</option>
        </select>
      </div>
    </form>
  </div>

  <section aria-labelledby="resultsHead">
    <h3 id="resultsHead">Results</h3>
    <p class="meta" id="resultCount"></p>
    <div id="results" class="grid"></div>
    <p id="emptyState" class="empty hidden">No matches. Try a broader term or clear the filters. <button class="secondary" id="clearFilters">Clear filters</button></p>
  </section>

  <section aria-labelledby="fotd">
    <h3 id="fotd">Fact of the day</h3>
    <p class="meta" id="factText"></p>
  </section>
</div>

<!-- TOPIC DETAIL -->
<div id="detail" class="hidden" aria-live="polite"></div>

<!-- STUDY -->
<div id="view-study" class="hidden">
  <div class="hero">
    <h2>Study tools</h2>
    <p class="meta">Flash cards are saved in this browser only. They are not synced or backed up. Use Export to keep a copy.</p>
    <form id="cardForm" class="panel" style="margin-top:0">
      <h3>New flash card</h3>
      <label for="front" class="meta">Front (question)</label>
      <input id="front" required maxlength="300">
      <label for="back" class="meta" style="display:block;margin-top:.5rem">Back (answer)</label>
      <textarea id="back" rows="2" required maxlength="800"></textarea>
      <div class="row" style="margin-top:.6rem">
        <button type="submit">Add card</button>
        <button type="button" class="secondary" id="exportBtn">Export my cards</button>
      </div>
    </form>
  </div>

  <div class="panel">
    <h3>Review due</h3>
    <p class="meta">Fixed intervals: 1, 3, 7, then 14 days. Mark a card as known to move it forward, or review again to reset it.</p>
    <div id="reviewArea"></div>
  </div>

  <div class="panel">
    <h3>All cards <span class="meta" id="cardTotal"></span></h3>
    <div id="cardList"></div>
  </div>
</div>

<!-- ABOUT -->
<div id="view-about" class="hidden panel">
  <h2>About WANE</h2>
  <p>WANE helps people explore neuroscience and neurosurgery at their own pace. Content is written and cited in small batches. Every page shows its review status.</p>
  <p class="draft">Content status: Draft, not yet reviewed by a qualified clinician or scientist.</p>
  <p><strong>Community guidelines:</strong> Comments are not available in this version. When they are added, comments are user-generated content and are never medical advice. Do not post identifiable patient information, medical records, or personal health details.</p>
  <p><strong>Privacy:</strong> This prototype collects no personal data. Flash cards and theme settings are stored in your browser only.</p>
</div>

<!-- LEGAL -->
<div id="view-legal" class="hidden panel">
  <h2>Disclaimer, terms, and privacy</h2>
  <h3>Disclaimer</h3>
  <p>WANE is an educational resource. It is not a substitute for a qualified clinician, medical training, or professional advice. It does not provide diagnosis or treatment recommendations and does not interpret any individual's scans or symptoms. Educational images and models must not be used for diagnosis or treatment.</p>
  <h3>Terms</h3>
  <p>Content is provided for learning. Citations are listed with each page. Verify any information before relying on it.</p>
  <h3>Privacy</h3>
  <p>No accounts and no tracking in this version. Local storage holds only your theme, level, and flash cards. Clearing your browser data removes them.</p>
  <h3>Phase 2 (not yet available)</h3>
  <p class="meta">3D models, case questions, comments, and accounts are planned for later releases.</p>
</div>

</main>

<footer>
  <p>WANE is an educational resource and not medical advice. &copy; WANE.</p>
</footer>

<script>
const TOPICS = [
  {id:"cortex-layers", title:"Layers of the cerebral cortex", type:"Topic", levels:["High School","Premed","Med School"], date:"2026-01-10",
   summary:"The cerebral cortex is organized into six layers, with differences in cell types and connections that vary across brain regions.",
   citations:["Kandel ER, Schwartz JH, Jessell TM, et al. Principles of Neural Science. McGraw-Hill. (Chapter on cortical organization.)"]},
  {id:"action-potential", title:"The action potential", type:"Topic", levels:["Curious","High School","Premed"], date:"2026-01-17",
   summary:"A neuron's action potential is a brief electrical event caused by the movement of sodium and potassium ions across the cell membrane.",
   citations:["Kandel ER, Schwartz JH, Jessell TM, et al. Principles of Neural Science. McGraw-Hill. (Chapter on the neuronal membrane potential.)"]},
  {id:"synapse", title:"Chemical synapses", type:"Topic", levels:["Curious","High School","Premed"], date:"2026-01-24",
   summary:"At a chemical synapse, a presynaptic neuron releases neurotransmitter that binds receptors on the postsynaptic cell, changing its activity.",
   citations:["Purves D, Augustine GJ, Fitzpatrick D, et al. Neuroscience. Sinauer Associates. (Chapter on synaptic transmission.)"]},
  {id:"blood-brain-barrier", title:"The blood-brain barrier", type:"Topic", levels:["Premed","Med School","Researcher"], date:"2026-02-02",
   summary:"Tight junctions between endothelial cells, along with astrocyte and pericyte support, limit which substances move from blood into brain tissue.",
   citations:["Abbott NJ, Patabendige AA, Dolman DE, Yusof SR, Begley DJ. Structure and function of the blood-brain barrier. Neurobiology of Disease. 2010. (Review article.)"]},
  {id:"broca-area", title:"Broca's area", type:"Terminology", levels:["High School","Premed","Med School"], date:"2026-02-09",
   summary:"Broca's area, in the inferior frontal lobe of the dominant hemisphere, is classically associated with speech production. Damage can cause expressive language difficulty.",
   citations:["Brodal P. The Central Nervous System: Structure and Function. Oxford University Press. (Chapter on language areas.)"]},
  {id:"hippocampus", title:"The hippocampus and memory", type:"Topic", levels:["Curious","High School","Researcher"], date:"2026-02-16",
   summary:"The hippocampus plays an important role in forming new declarative memories. Its exact mechanisms remain an active area of research.",
   citations:["Squire LR. Memory and the hippocampus: a synthesis from findings with rats, monkeys, and humans. Psychological Review. 1992. (Review article.)"]},
  {id:"csf", title:"Cerebrospinal fluid circulation", type:"Topic", levels:["High School","Premed","Med School"], date:"2026-02-23",
   summary:"Cerebrospinal fluid is produced mainly by the choroid plexus within the ventricles and circulates through the ventricles and subarachnoid space.",
   citations:["Brodal P. The Central Nervous System: Structure and Function. Oxford University Press. (Chapter on cerebrospinal fluid.)"]},
  {id:"gcs", title:"Glasgow Coma Scale", type:"Terminology", levels:["Premed","Med School"], date:"2026-03-02",
   summary:"The Glasgow Coma Scale scores eye opening, verbal response, and motor response to describe a person's level of consciousness. It is a clinical tool used by trained staff.",
   citations:["Teasdale G, Jennett B. Assessment of coma and impaired consciousness: a practical scale. The Lancet. 1974. (Original description.)"]},
  {id:"craniotomy", title:"Craniotomy (overview)", type:"Procedure", levels:["Med School","Researcher","Lecturer"], date:"2026-03-09",
   summary:"A craniotomy is a surgical opening in the skull to access the brain. This overview is educational only and does not describe how any individual patient should be treated.",
   citations:["Placeholder: citation pending verification against a neurosurgical textbook or PubMed review."]},
  {id:"mri-basics", title:"MRI basics", type:"Imaging", levels:["Curious","High School","Lecturer"], date:"2026-03-16",
   summary:"Magnetic resonance imaging uses strong magnetic fields and radio waves to produce detailed images of soft tissue. Image interpretation requires trained clinicians.",
   citations:["Placeholder: citation pending verification against a radiology textbook or review article."]}
];

const FACTS = [
  "Your brain uses roughly 20 percent of your body's resting energy, despite being about 2 percent of its weight.",
  "Neurons are not the only cells in the brain. Glial cells outnumber neurons in many regions, though the exact ratio varies.",
  "The adult human brain contains on the order of 86 billion neurons, a commonly cited estimate."
];

const LS = {level:"wane.level", theme:"wane.theme", cards:"wane.cards"};
let state = { level:"", cards: JSON.parse(localStorage.getItem(LS.cards) || "[]") };
const $ = s => document.querySelector(s);
const esc = s => String(s).replace(/[&<>"']/g, c => ({"&":"&amp;","<":"&lt;",">":"&gt;",'"':"&quot;","'":"&#39;"}[c]));

// Theme
function applyTheme(t){ document.documentElement.setAttribute("data-theme", t); $("#themeSel").value = t; }
applyTheme(localStorage.getItem(LS.theme) || "system");
$("#themeSel").addEventListener("change", e => { localStorage.setItem(LS.theme, e.target.value); applyTheme(e.target.value); });

// Level
function setLevel(l){
  state.level = l; localStorage.setItem(LS.level, l);
  document.querySelectorAll("[data-level]").forEach(b => {
    const on = b.dataset.level === l; b.classList.toggle("active", on); b.setAttribute("aria-pressed", on);
  });
  $("#levelNote").textContent = l ? `Showing content suited to ${l}. Click the level again to clear it.` : "No level selected. Showing all content. You can change your level at any time.";
  $("#fLevel").value = l;
  render();
}
document.querySelectorAll("[data-level]").forEach(b => b.addEventListener("click", () => setLevel(state.level === b.dataset.level ? "" : b.dataset.level)));
$("#fLevel").addEventListener("change", e => setLevel(e.target.value));
setLevel(localStorage.getItem(LS.level) || "");

// Search and render
function filtered(){
  const q = $("#q").value.trim().toLowerCase();
  const t = $("#fType").value, lv = $("#fLevel").value, d = $("#fDate").value;
  let list = TOPICS.filter(x =>
    (!q || (x.title + " " + x.summary).toLowerCase().includes(q)) &&
    (!t || x.type === t) &&
    (!lv || x.levels.includes(lv))
  );
  if (d === "newest") list.sort((a,b)=> b.date.localeCompare(a.date));
  if (d === "oldest") list.sort((a,b)=> a.date.localeCompare(b.date));
  return list;
}
function render(){
  const list = filtered();
  $("#results").innerHTML = list.map(x => `
    <article class="card" tabindex="0" role="button" data-id="${x.id}" aria-label="Open ${esc(x.title)}">
      <span class="badge">${esc(x.type)}</span>
      <h4>${esc(x.title)}</h4>
      <p class="meta">${esc(x.summary).slice(0,110)}...</p>
      <p class="meta">${x.levels.map(esc).join(" · ")} · ${esc(x.date)}</p>
      <span class="draft">Draft, not yet reviewed</span>
    </article>`).join("");
  $("#resultCount").textContent = `${list.length} of ${TOPICS.length} resources`;
  $("#emptyState").classList.toggle("hidden", list.length > 0);
  document.querySelectorAll(".card[data-id]").forEach(c => {
    const open = () => openTopic(c.dataset.id);
    c.addEventListener("click", open);
    c.addEventListener("keydown", e => { if (e.key === "Enter" || e.key === " ") { e.preventDefault(); open(); } });
  });
}
["#q","#fType","#fDate"].forEach(s => $(s).addEventListener("input", render));
$("#fLevel").addEventListener("change", render);
$("#searchForm").addEventListener("submit", e => e.preventDefault());
$("#clearFilters").addEventListener("click", () => { $("#q").value=""; $("#fType").value=""; $("#fDate").value=""; setLevel(""); });

// Topic detail
function openTopic(id){
  const x = TOPICS.find(t => t.id === id); if(!x) return;
  $("#detail").innerHTML = `
    <p><button class="secondary" id="back">← Back to results</button></p>
    <span class="badge">${esc(x.type)}</span>
    <h2>${esc(x.title)}</h2>
    <p class="meta">Learning level: ${x.levels.map(esc).join(", ")} · Published: ${esc(x.date)} · Source: WANE draft</p>
    <span class="draft">Draft, not yet reviewed. Last reviewed: none.</span>
    <p>${esc(x.summary)}</p>
    <h3>Citations</h3>
    <ul>${x.citations.map(c => `<li>${esc(c)}</li>`).join("")}</ul>
    <p class="meta">License: citations are references only. No copyrighted text is reproduced.</p>
    <div class="disclaimer">WANE is an educational resource. It is not a substitute for a qualified clinician, medical training, or professional advice.</div>`;
  $("#detail").classList.remove("hidden");
  $("#view-home").classList.add("hidden");
  $("#back").addEventListener("click", closeTopic);
  $("#detail").focus?.();
  window.scrollTo(0,0);
}
function closeTopic(){ $("#detail").classList.add("hidden"); $("#view-home").classList.remove("hidden"); }

// Views
function show(v){
  ["home","study","about","legal"].forEach(n => $("#view-"+n)?.classList.toggle("hidden", n !== v));
  if (v !== "home") { $("#detail").classList.add("hidden"); }
  else { $("#detail").classList.add("hidden"); }
  if (v === "study") renderStudy();
}
document.querySelectorAll("nav a").forEach(a => a.addEventListener("click", e => { e.preventDefault(); show(a.dataset.view); }));

// Fact of the day (deterministic by date, not a pop-up)
const dayIdx = Math.floor(Date.now() / 86400000) % FACTS.length;
$("#factText").textContent = FACTS[dayIdx];

// Flash cards with fixed intervals (days)
const INTERVALS = [1,3,7,14];
function saveCards(){ localStorage.setItem(LS.cards, JSON.stringify(state.cards)); }
$("#cardForm").addEventListener("submit", e => {
  e.preventDefault();
  state.cards.push({ id: Date.now().toString(36), front: $("#front").value.trim(), back: $("#back").value.trim(), stage: 0, due: Date.now() });
  saveCards(); $("#cardForm").reset(); renderStudy();
});
function review(id, known){
  const c = state.cards.find(x => x.id === id); if (!c) return;
  c.stage = known ? Math.min(c.stage + 1, INTERVALS.length - 1) : 0;
  c.due = Date.now() + INTERVALS[c.stage] * 86400000;
  saveCards(); renderStudy();
}
function renderStudy(){
  const now = Date.now();
  const due = state.cards.filter(c => c.due <= now);
  $("#reviewArea").innerHTML = due.length ? due.map(c => `
    <div class="card-item">
      <p><strong>${esc(c.front)}</strong></p>
      <details><summary>Show answer</summary><p>${esc(c.back)}</p></details>
      <div class="row" style="margin-top:.4rem">
        <button data-known="${c.id}">Known</button>
        <button class="secondary" data-again="${c.id}">Review again</button>
      </div>
    </div>`).join("") : `<p class="empty">Nothing due right now.</p>`;
  $("#cardList").innerHTML = state.cards.length ? state.cards.map(c => `
    <div class="card-item">
      <p><strong>${esc(c.front)}</strong></p>
      <p class="meta">${esc(c.back)}</p>
      <p class="meta">Next review: ${new Date(c.due).toLocaleDateString()}</p>
      <button class="secondary" data-del="${c.id}">Delete</button>
    </div>`).join("") : `<p class="empty">No cards yet. Add one above.</p>`;
  $("#cardTotal").textContent = `(${state.cards.length})`;
  document.querySelectorAll("[data-known]").forEach(b => b.onclick = () => review(b.dataset.known, true));
  document.querySelectorAll("[data-again]").forEach(b => b.onclick = () => review(b.dataset.again, false));
  document.querySelectorAll("[data-del]").forEach(b => b.onclick = () => { state.cards = state.cards.filter(c => c.id !== b.dataset.del); saveCards(); renderStudy(); });
}
$("#exportBtn").addEventListener("click", () => {
  const blob = new Blob([JSON.stringify(state.cards, null, 2)], {type:"application/json"});
  const a = Object.assign(document.createElement("a"), {href: URL.createObjectURL(blob), download: "wane-flashcards.json"});
  a.click(); URL.revokeObjectURL(a.href);
});

render();
</script>
</body>
</html>
