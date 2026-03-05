<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>rafa mass · readme preview</title>
<link href="https://fonts.googleapis.com/css2?family=EB+Garamond:ital,wght@0,400;0,500;1,400&family=JetBrains+Mono:wght@400;500&display=swap" rel="stylesheet">
<style>
  :root {
    --bg: #0d0d0d;
    --surface: #141414;
    --border: #232323;
    --text: #d4cfc7;
    --muted: #5a564f;
    --accent: #c9a96e;
    --code-bg: #1a1a1a;
  }

  * { box-sizing: border-box; margin: 0; padding: 0; }

  body {
    background: var(--bg);
    color: var(--text);
    font-family: 'EB Garamond', Georgia, serif;
    font-size: 18px;
    line-height: 1.7;
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 3rem 1.5rem;
  }

  .shell {
    width: 100%;
    max-width: 660px;
  }


  /* --- lang toggle --- */
  .lang-bar {
    display: flex;
    gap: .4rem;
    margin-bottom: 2.5rem;
    justify-content: flex-end;
  }

  .lang-btn {
    background: none;
    border: none;
    font-size: 1.3rem;
    cursor: pointer;
    opacity: .35;
    transition: opacity .2s, transform .15s;
    line-height: 1;
    padding: .2rem;
  }

  .lang-btn:hover { opacity: .7; transform: scale(1.15); }
  .lang-btn.active { opacity: 1; transform: scale(1.2); }

  /* --- content --- */
  .readme { animation: fadein .35s ease; }

  @keyframes fadein {
    from { opacity: 0; transform: translateY(6px); }
    to   { opacity: 1; transform: translateY(0); }
  }

  .epigraph {
    text-align: center;
    margin-bottom: 2.5rem;
  }

  .epigraph code {
    display: inline-block;
    font-family: 'JetBrains Mono', monospace;
    font-size: .85rem;
    color: var(--accent);
    background: var(--code-bg);
    border: 1px solid var(--border);
    padding: .6rem 1.4rem;
    letter-spacing: .04em;
  }

  hr {
    border: none;
    border-top: 1px solid var(--border);
    margin: 2rem 0;
  }

  h2 {
    font-family: 'JetBrains Mono', monospace;
    font-size: .72rem;
    letter-spacing: .14em;
    text-transform: uppercase;
    color: var(--muted);
    font-weight: 400;
    margin-bottom: 1rem;
  }

  p { margin-bottom: .9rem; }
  p:last-child { margin-bottom: 0; }

  em { color: var(--accent); font-style: italic; }

  .footer {
    text-align: center;
    margin-top: 2.5rem;
    font-family: 'JetBrains Mono', monospace;
    font-size: .7rem;
    color: var(--muted);
    letter-spacing: .08em;
  }


</style>
</head>
<body>
<div class="shell">

  <div class="lang-bar">
    <button class="lang-btn active" onclick="setLang('ptbr')" title="Português BR">🇧🇷</button>
    <button class="lang-btn" onclick="setLang('en')" title="English GB">🇬🇧</button>
    <button class="lang-btn" onclick="setLang('es')" title="Español">🇪🇸</button>
    <button class="lang-btn" onclick="setLang('fr')" title="Français">🇫🇷</button>
  </div>


  <div class="readme" id="readme-content"></div>

</div>

<script>
const content = {
  dfw: {
    ptbr: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>escritor. professor de língua portuguesa.<br>
que também — e isso importa, embora seja difícil explicar exatamente <em>por que</em> importa — aprendeu a conversar com máquinas.</p>
<p>não é dev. isso não é modéstia performática: é uma distinção técnica com consequências reais.<br>
é alguém que viba, itera, publica o que funciona e deixa visível o que não funcionou ainda,<br>
porque a ilusão de competência contínua é, no fundo, o oposto do que interessa aqui.</p>`,
      projects: `<p>projetos feitos por curiosidade genuína — que é diferente de curiosidade exibida.<br>
ferramentas que precisavam existir e não existiam do jeito certo.<br>
coisas que começaram como aula e, por razões que o próprio autor não soube prever, viraram código.</p>`,
      contact: `<p>se quiser conversar sobre língua, ensino, ou qualquer coisa que não caiba numa issue →<br>
abre uma issue mesmo. ou me acha onde me achar.</p>`,
      h_projects: "o que você encontra por aqui",
      h_contact: "contato",
      footer: "feito com atenção"
    },
    en: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>writer. teacher of the portuguese language.<br>
who also — and this matters, though it's genuinely hard to articulate <em>why</em> it matters — learned to talk to machines.</p>
<p>not a dev. that's not performative modesty: it's a technical distinction with real consequences.<br>
someone who vibes, iterates, ships what works and leaves visible what hasn't worked yet,<br>
because the illusion of continuous competence is, at bottom, the opposite of what's interesting here.</p>`,
      projects: `<p>projects made out of genuine curiosity — which is different from displayed curiosity.<br>
tools that needed to exist and didn't exist quite right.<br>
things that started as lessons and, for reasons the author himself didn't foresee, became code.</p>`,
      contact: `<p>if you want to talk about language, teaching, or anything that doesn't fit in an issue →<br>
open an issue anyway. or find me where you find me.</p>`,
      h_projects: "what you'll find here",
      h_contact: "contact",
      footer: "made with attention"
    },
    es: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>escritor. profesor de lengua portuguesa.<br>
que también — y esto importa, aunque sea difícil explicar exactamente <em>por qué</em> importa — aprendió a conversar con máquinas.</p>
<p>no es dev. eso no es modestia performativa: es una distinción técnica con consecuencias reales.<br>
es alguien que vibe, itera, publica lo que funciona y deja visible lo que aún no funcionó,<br>
porque la ilusión de competencia continua es, en el fondo, lo opuesto de lo que interesa aquí.</p>`,
      projects: `<p>proyectos hechos por curiosidad genuina — que es distinta de la curiosidad exhibida.<br>
herramientas que necesitaban existir y no existían de la manera correcta.<br>
cosas que empezaron como clase y, por razones que el propio autor no supo prever, se convirtieron en código.</p>`,
      contact: `<p>si quieres hablar sobre lengua, enseñanza, o cualquier cosa que no quepa en un issue →<br>
abre un issue de todas formas. o encuéntrame donde me encuentres.</p>`,
      h_projects: "qué encontrarás aquí",
      h_contact: "contacto",
      footer: "hecho con atención"
    },
    fr: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>écrivain. professeur de langue portugaise.<br>
qui a aussi — et cela compte, même s'il est difficile d'expliquer exactement <em>pourquoi</em> cela compte — appris à parler aux machines.</p>
<p>pas un dev. ce n'est pas de la fausse modestie : c'est une distinction technique avec des conséquences réelles.<br>
quelqu'un qui vibe, itère, publie ce qui fonctionne et laisse visible ce qui n'a pas encore fonctionné,<br>
parce que l'illusion de compétence continue est, au fond, le contraire de ce qui intéresse ici.</p>`,
      projects: `<p>projets faits par curiosité véritable — ce qui est différent de la curiosité exhibée.<br>
des outils qui devaient exister et n'existaient pas de la bonne manière.<br>
des choses qui ont commencé comme des cours et, pour des raisons que l'auteur lui-même n'avait pas prévues, sont devenues du code.</p>`,
      contact: `<p>si vous voulez parler de langue, d'enseignement, ou de quoi que ce soit qui ne rentre pas dans un issue →<br>
ouvrez un issue quand même. ou trouvez-moi où vous me trouverez.</p>`,
      h_projects: "ce que vous trouverez ici",
      h_contact: "contact",
      footer: "fait avec attention"
    }
  },
  gaiman: {
    ptbr: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>há pessoas que ensinam línguas e há pessoas que as habitam.<br>
rafa mass é do segundo tipo — escritor, professor, alguém que um dia descobriu<br>
que as máquinas também gostam de uma boa história,<br>
e decidiu ver aonde isso levava.</p>
<p>não chegou aqui pelo caminho óbvio. veio pelas artes, pela história, pela sala de aula.<br>
aprendeu a vibar código como quem aprende um dialeto novo numa cidade estranha:<br>
com atenção, com erro, com a disposição de ficar.</p>`,
      projects: `<p>ferramentas nascidas de necessidade real.<br>
experimentos que começaram como pergunta e viraram projeto.<br>
coisas feitas para durar — ou pelo menos para ensinar algo ao cair.</p>`,
      contact: `<p>toda boa história começa com alguém que resolve falar →<br>
abre uma issue. ou me acha onde me achar.</p>`,
      h_projects: "o que você encontra por aqui",
      h_contact: "contato",
      footer: "feito com atenção"
    },
    en: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>there are people who teach languages and people who inhabit them.<br>
rafa mass is the second kind — a writer, a teacher, someone who discovered one day<br>
that machines also appreciate a good story,<br>
and decided to see where that led.</p>
<p>he didn't arrive here by the obvious road. he came through art, through history, through the classroom.<br>
he learned to vibe code the way one learns a new dialect in a strange city:<br>
with attention, with mistakes, with the willingness to stay.</p>`,
      projects: `<p>tools born from genuine need.<br>
experiments that started as questions and became projects.<br>
things made to last — or at least to teach something when they fall.</p>`,
      contact: `<p>every good story begins with someone who decides to speak →<br>
open an issue. or find me where you find me.</p>`,
      h_projects: "what you'll find here",
      h_contact: "contact",
      footer: "made with attention"
    },
    es: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>hay personas que enseñan lenguas y hay personas que las habitan.<br>
rafa mass es del segundo tipo — escritor, profesor, alguien que un día descubrió<br>
que las máquinas también aprecian una buena historia,<br>
y decidió ver adónde llevaba eso.</p>
<p>no llegó aquí por el camino obvio. llegó por las artes, por la historia, por el aula.<br>
aprendió a vibear código como quien aprende un nuevo dialecto en una ciudad extraña:<br>
con atención, con error, con la disposición de quedarse.</p>`,
      projects: `<p>herramientas nacidas de necesidad real.<br>
experimentos que empezaron como pregunta y se convirtieron en proyecto.<br>
cosas hechas para durar — o al menos para enseñar algo al caer.</p>`,
      contact: `<p>toda buena historia comienza con alguien que decide hablar →<br>
abre un issue. o encuéntrame donde me encuentres.</p>`,
      h_projects: "qué encontrarás aquí",
      h_contact: "contacto",
      footer: "hecho con atención"
    },
    fr: {
      epigraph: "de tudo, ao meu amor serei atento",
      intro: `<p><strong>rafa mass</strong></p>
<p>il y a des gens qui enseignent les langues et des gens qui les habitent.<br>
rafa mass est du deuxième type — écrivain, professeur, quelqu'un qui a découvert un jour<br>
que les machines apprécient elles aussi une bonne histoire,<br>
et a décidé de voir où cela menait.</p>
<p>il n'est pas arrivé ici par le chemin évident. il est venu par les arts, par l'histoire, par la salle de classe.<br>
il a appris à vibe coder comme on apprend un nouveau dialecte dans une ville étrangère :<br>
avec attention, avec erreur, avec la disposition de rester.</p>`,
      projects: `<p>des outils nés d'un besoin réel.<br>
des expériences qui ont commencé comme des questions et sont devenues des projets.<br>
des choses faites pour durer — ou du moins pour enseigner quelque chose en tombant.</p>`,
      contact: `<p>toute bonne histoire commence par quelqu'un qui décide de parler →<br>
ouvrez un issue. ou trouvez-moi où vous me trouverez.</p>`,
      h_projects: "ce que vous trouverez ici",
      h_contact: "contact",
      footer: "fait avec attention"
    }
  }
};

let currentLang = 'ptbr';

function render() {
  const d = content.dfw[currentLang];
  const el = document.getElementById('readme-content');

  el.innerHTML = `
    <div class="epigraph"><code>${d.epigraph}</code></div>
    <hr>
    <div>${d.intro}</div>
    <hr>
    <h2>${d.h_projects}</h2>
    <div>${d.projects}</div>
    <hr>
    <h2>${d.h_contact}</h2>
    <div>${d.contact}</div>
    <div class="footer">${d.footer}</div>
  `;

  el.style.animation = 'none';
  el.offsetHeight;
  el.style.animation = 'fadein .35s ease';
}

function setLang(l) {
  currentLang = l;
  document.querySelectorAll('.lang-btn').forEach(b => b.classList.remove('active'));
  document.querySelector(`.lang-btn[onclick="setLang('${l}')"]`).classList.add('active');
  render();
}

render();
</script>
</body>
</html>
