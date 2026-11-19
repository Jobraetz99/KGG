<!DOCTYPE html>
<html lang="de">
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>KGG-Rechner</title>
<link href="https://fonts.googleapis.com/css2?family=Fira+Sans:wght@400;500;700&display=swap" rel="stylesheet">
<style>
  :root{--red:#AE3E3D;--red2:#C86E62;--pink:#F6E3E0;--grey:#DADFE1;--ink:#2B2B2B;--mute:#6b6b6b;--green:#3E8E5A}
  *{box-sizing:border-box}
  body{margin:0;font-family:"Fira Sans",system-ui,sans-serif;color:var(--ink);background:#faf7f6}
  header{background:var(--red);color:#fff;padding:20px 20px 18px}
  header small{letter-spacing:.12em;text-transform:uppercase;font-size:12px;opacity:.85}
  header h1{margin:4px 0 0;font-size:26px;font-weight:700}
  main{max-width:760px;margin:0 auto;padding:16px}
  .card{background:#fff;border-radius:14px;padding:16px;margin-bottom:14px;box-shadow:0 1px 3px rgba(0,0,0,.06)}
  h2{font-size:15px;text-transform:uppercase;letter-spacing:.06em;color:var(--red);margin:0 0 12px}
  .presets{display:flex;gap:8px;flex-wrap:wrap;margin-bottom:4px}
  .presets button{border:1.5px solid var(--red);background:#fff;color:var(--red);border-radius:999px;padding:7px 14px;font:500 14px "Fira Sans";cursor:pointer}
  .presets button.on{background:var(--red);color:#fff}
  .grid{display:grid;grid-template-columns:1fr 1fr;gap:12px}
  label{display:block;font-size:13px;color:var(--mute);margin-bottom:4px}
  input[type=number]{width:100%;padding:10px;border:1.5px solid var(--grey);border-radius:10px;font:500 17px "Fira Sans";color:var(--ink)}
  input[type=number]:focus{outline:none;border-color:var(--red2)}
  .slider{margin-top:6px}
  .slider .val{font-size:34px;font-weight:700;color:var(--red)}
  .slider .val span{font-size:16px;color:var(--mute);font-weight:400}
  input[type=range]{width:100%;accent-color:var(--red);height:28px}
  .kpis{display:grid;grid-template-columns:1fr 1fr;gap:10px}
  .kpi{background:var(--pink);border-radius:12px;padding:12px}
  .kpi .l{font-size:12.5px;color:var(--mute)}
  .kpi .v{font-size:24px;font-weight:700;margin-top:2px}
  .kpi.big{grid-column:1/-1;background:var(--red);color:#fff}
  .kpi.big .l{color:#fff;opacity:.85}
  .kpi.big .v{font-size:32px}
  .bars .row{display:grid;grid-template-columns:120px 1fr 78px;align-items:center;gap:8px;margin:7px 0;font-size:14px}
  .bars .track{background:#f1eeed;border-radius:6px;height:22px;overflow:hidden}
  .bars .fill{height:100%;background:var(--grey);border-radius:6px;transition:width .25s}
  .bars .row.kgg .fill{background:var(--red)}
  .bars .row.kgg{font-weight:700}
  .bars .num{text-align:right;font-variant-numeric:tabular-nums}
  .note{font-size:12px;color:var(--mute);line-height:1.45;margin-top:10px}
  .verdict{margin-top:10px;font-size:15px;font-weight:500;padding:10px 12px;border-radius:10px;background:#f4f4f4}
  @media (max-width:520px){.grid{grid-template-columns:1fr 1fr}.bars .row{grid-template-columns:96px 1fr 70px}}
</style>
</head>
<body>
<header><small>Krankengymnastik am Gerät</small><h1>KGG-Rechner</h1></header>
<main>
  <section class="card">
    <h2>Eure Ausstattung</h2>
    <div class="presets" id="presets">
      <button data-p="A" class="on">Basic · 20.000 €</button>
      <button data-p="B">Premium · 60.000 €</button>
    </div>
  </section>

  <section class="card">
    <h2>Wie viele Patienten pro KGG-Stunde?</h2>
    <div class="slider">
      <div class="val"><b id="patOut">2,0</b> <span>Patienten parallel (Ø)</span></div>
      <input type="range" id="pat" min="1" max="3" step="0.1" value="1">
    </div>
    <div class="grid" style="margin-top:8px">
      <div><label for="std">KGG-Stunden pro Monat</label><input type="number" id="std" value="60" min="0" step="1"></div>
      <div><label for="pk">Personalkosten pro Stunde (€)</label><input type="number" id="pk" value="30" min="0" step="1"></div>
    </div>
  </section>

  <section class="card">
    <h2>Ergebnis</h2>
    <div class="kpis">
      <div class="kpi big"><div class="l">Ergebnis KGG pro Monat (nach Gerät, Raum, Personal)</div><div class="v" id="res">–</div></div>
      <div class="kpi"><div class="l">Deckungsbeitrag pro Stunde</div><div class="v" id="db">–</div></div>
      <div class="kpi"><div class="l">Break-even</div><div class="v" id="be">–</div></div>
      <div class="kpi"><div class="l">Umsatz pro Stunde</div><div class="v" id="ums">–</div></div>
      <div class="kpi"><div class="l">Fixkosten pro Monat</div><div class="v" id="fix">–</div></div>
    </div>
    <div class="verdict" id="verdict"></div>
  </section>

  <section class="card">
    <h2>Was bringt eine Therapeutenstunde?</h2>
    <div class="bars" id="bars"></div>
    <div class="note">Deckungsbeitrag = Umsatz pro Stunde minus Personalkosten, vor Raum, Gerät und Verwaltung. KG und MT im 20-Minuten-Takt (3 Behandlungen pro Stunde).</div>
  </section>

  <section class="card">
    <h2>Kosten (anpassbar)</h2>
    <div class="grid">
      <div><label for="inv">Investition Ausstattung (€)</label><input type="number" id="inv" value="20000" min="0" step="1000"></div>
      <div><label for="jahre">Abschreibung (Jahre)</label><input type="number" id="jahre" value="5" min="1" step="1"></div>
      <div><label for="miete">Raummiete inkl. NK / Monat (€)</label><input type="number" id="miete" value="300" min="0" step="10"></div>
      <div><label for="preis">Preis KGG pro Patient (€)</label><input type="number" id="preis" value="55.81" min="0" step="0.01"></div>
    </div>
    <div class="note">Preise: GKV-Vergütung bundesweit ab 01.01.2026 – KG-Gerät (X0507) 55,81 €, KG (X0501) 29,63 €, MT 35,59 €. Vereinfachte Rechnung für die Fortbildung, ohne Ausfälle, Verwaltung und Steuern.</div>
  </section>
</main>
<script>
const KG=29.63*3, MT=35.59*3;
const presets={
  A:{inv:20000,miete:300},
  B:{inv:60000,miete:300}
};
const $=id=>document.getElementById(id);
const eur=(v,d=0)=>v.toLocaleString('de-DE',{minimumFractionDigits:d,maximumFractionDigits:d})+' €';
function num(id){const v=parseFloat($(id).value);return isNaN(v)?0:v}
function calc(){
  const pat=num('pat'),std=num('std'),pk=num('pk'),inv=num('inv'),jahre=Math.max(1,num('jahre')),miete=num('miete'),preis=num('preis');
  $('patOut').textContent=pat.toLocaleString('de-DE',{minimumFractionDigits:1,maximumFractionDigits:1});
  const fix=inv/(jahre*12)+miete, ums=pat*preis, db=ums-pk, res=std*db-fix;
  $('fix').textContent=eur(fix); $('ums').textContent=eur(ums,2); $('db').textContent=eur(db,2);
  $('be').textContent=db>0?Math.ceil(fix/db)+' Std./Monat':'nie';
  $('res').textContent=(res>0?'+':'')+eur(res);
  const kgDb=KG-pk;
  let v;
  if(db<=0) v='❌ Jede KGG-Stunde kostet Geld.';
  else if(db<kgDb) v='⚠️ Eine normale KG-Stunde bringt mehr ('+eur(kgDb,2)+'). Ziel: mehr Patienten pro Stunde.';
  else v='✅ Besser als eine KG-Stunde – um '+eur(db-kgDb,2)+' pro Stunde.';
  $('verdict').textContent=v;
  const rows=[['KGG (Ihr Fall)',db,true],['KG 20 Min.',KG-pk],['MT 20 Min.',MT-pk],['KGG 1 Patient',preis-pk],['KGG 3 Patienten',3*preis-pk]];
  const max=Math.max(...rows.map(r=>r[1]),1);
  $('bars').innerHTML=rows.map(r=>`<div class="row${r[2]?' kgg':''}"><div>${r[0]}</div><div class="track"><div class="fill" style="width:${Math.max(0,r[1])/max*100}%"></div></div><div class="num">${eur(r[1],2)}</div></div>`).join('');
}
function apply(p){const s=presets[p];for(const k in s)$(k).value=s[k];document.querySelectorAll('#presets button').forEach(b=>b.classList.toggle('on',b.dataset.p===p));calc()}
document.querySelectorAll('input').forEach(i=>i.addEventListener('input',()=>{if(i.id==='inv'||i.id==='miete')document.querySelectorAll('#presets button').forEach(b=>b.classList.remove('on'));calc()}));
document.querySelectorAll('#presets button').forEach(b=>b.addEventListener('click',()=>apply(b.dataset.p)));
apply('A');
</script>
</body>
</html>
