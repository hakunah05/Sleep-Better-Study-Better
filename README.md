<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1.0" />
  <title>Sleep Better • Study Better • UVic Sleep Guide </title>
  <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css">
  <style>
    :root{
      --bg:#0b1220;
      --bg-soft:#111b2e;
      --panel:#172338;
      --panel-2:#1f2d46;
      --text:#e5eefb;
      --muted:#b6c3d9;
      --accent:#63e6e2;
      --accent-2:#f59e0b;
      --accent-3:#f97316;
      --border:rgba(255,255,255,0.08);
      --shadow:0 18px 50px rgba(0,0,0,0.35);
      --radius:22px;
      --radius-sm:14px;
    }

    *{box-sizing:border-box;margin:0;padding:0}
    html{scroll-behavior:smooth}
    body{
      font-family:"Segoe UI", Arial, sans-serif;
      background:
        radial-gradient(circle at top left, rgba(107,33,168,0.24), transparent 28%),
        radial-gradient(circle at top right, rgba(14,165,233,0.18), transparent 24%),
        linear-gradient(180deg, #0b1220 0%, #0f172a 48%, #111827 100%);
      color:var(--text);
      line-height:1.7;
    }

    a{color:var(--accent);text-decoration:none}
    a:hover{text-decoration:underline}

    .container{
      width:min(1200px, 92%);
      margin:0 auto;
    }

    header{
      position:relative;
      overflow:hidden;
      padding:5.8rem 1rem 4.5rem;
      text-align:center;
      background:
        linear-gradient(135deg, rgba(30,41,59,0.95) 0%, rgba(91,33,182,0.82) 48%, rgba(8,145,178,0.88) 100%);
      border-bottom:1px solid rgba(255,255,255,0.08);
      box-shadow:var(--shadow);
    }

    header::before{
      content:"";
      position:absolute;
      inset:0;
      background:
        radial-gradient(circle at 20% 18%, rgba(252,211,77,0.26), transparent 18%),
        radial-gradient(circle at 82% 22%, rgba(255,255,255,0.12), transparent 10%),
        radial-gradient(circle at 50% 80%, rgba(103,232,249,0.14), transparent 22%);
      pointer-events:none;
    }

    .hero-content{
      position:relative;
      z-index:2;
      max-width:1000px;
      margin:0 auto;
    }

    .eyebrow{
      display:inline-block;
      font-size:0.95rem;
      letter-spacing:.12em;
      text-transform:uppercase;
      color:#fde68a;
      font-weight:800;
      margin-bottom:1rem;
    }

    h1{
      font-size:clamp(2.1rem, 4.2vw, 4rem);
      line-height:1.15;
      margin-bottom:1rem;
    }

    .hero-sub{
      font-size:1.12rem;
      color:#f3f7ff;
      max-width:900px;
      margin:0 auto 1.8rem;
    }

    .hero-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(180px,1fr));
      gap:1rem;
      margin-top:2rem;
    }

    .hero-stat{
      background:rgba(255,255,255,0.08);
      border:1px solid rgba(255,255,255,0.1);
      border-radius:18px;
      padding:1rem;
      backdrop-filter:blur(4px);
    }

    .hero-stat strong{
      display:block;
      font-size:1.6rem;
      color:#fff;
    }

    .hero-actions{
      display:flex;
      flex-wrap:wrap;
      gap:1rem;
      justify-content:center;
      margin-top:2rem;
    }

    .btn{
      display:inline-flex;
      align-items:center;
      gap:.7rem;
      background:var(--accent);
      color:#082032;
      border:none;
      border-radius:999px;
      padding:1rem 1.45rem;
      font-size:1rem;
      font-weight:800;
      cursor:pointer;
      transition:.25s ease;
      box-shadow:0 10px 24px rgba(0,0,0,0.18);
    }

    .btn:hover{
      transform:translateY(-2px);
      background:var(--accent-3);
      color:#fff;
    }

    .btn.secondary{
      background:rgba(255,255,255,0.12);
      color:#fff;
      border:1px solid rgba(255,255,255,0.15);
    }

    nav{
      position:sticky;
      top:0;
      z-index:999;
      background:rgba(13,20,35,0.88);
      backdrop-filter:blur(10px);
      border-bottom:1px solid var(--border);
      box-shadow:0 10px 22px rgba(0,0,0,0.22);
    }

    .nav-inner{
      width:min(1250px,95%);
      margin:0 auto;
      padding:0.95rem .5rem;
      display:flex;
      flex-wrap:wrap;
      justify-content:center;
      gap:.75rem 1.2rem;
    }

    nav a{
      color:#d8f9ff;
      font-size:.98rem;
      font-weight:700;
      padding:.45rem .8rem;
      border-radius:999px;
      transition:.2s ease;
    }

    nav a:hover{
      background:rgba(99,230,226,0.12);
      text-decoration:none;
      color:#fff;
    }

    section{
      margin:2rem auto;
      padding:2.3rem;
      background:linear-gradient(180deg, rgba(23,35,56,0.96), rgba(17,27,46,0.96));
      border:1px solid var(--border);
      border-radius:var(--radius);
      box-shadow:var(--shadow);
    }

    .section-title{
      display:flex;
      align-items:center;
      gap:.8rem;
      margin-bottom:.8rem;
    }

    .section-title i{
      color:var(--accent);
      font-size:1.4rem;
    }

    h2{
      font-size:clamp(1.55rem, 2.4vw, 2.5rem);
      color:var(--accent);
      line-height:1.2;
    }

    .section-intro{
      color:var(--muted);
      margin:0.5rem 0 1.5rem;
      font-size:1.02rem;
    }

    .callout{
      background:linear-gradient(135deg, rgba(99,230,226,0.08), rgba(245,158,11,0.08));
      border:1px solid rgba(99,230,226,0.16);
      border-left:6px solid var(--accent-3);
      padding:1rem 1.1rem;
      border-radius:16px;
      margin:1rem 0 1.5rem;
      color:#e8f7ff;
    }

    .grid-2{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(280px,1fr));
      gap:1.2rem;
    }

    .grid-3{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:1rem;
    }

    .info-box{
      background:var(--panel-2);
      border:1px solid var(--border);
      border-radius:18px;
      padding:1.1rem 1rem;
    }

    .info-box h3{
      color:#fff;
      margin-bottom:.45rem;
      font-size:1.08rem;
    }

    .info-box p,
    .info-box li{
      color:var(--muted);
      font-size:.98rem;
    }

    .video-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(300px,1fr));
      gap:1.3rem;
      margin-top:1.2rem;
    }

    .video-card{
      background:var(--panel-2);
      border:1px solid var(--border);
      border-radius:20px;
      padding:1rem;
      box-shadow:0 10px 26px rgba(0,0,0,0.22);
    }

    .video-card h3{
      font-size:1.02rem;
      color:#fff;
      margin-bottom:.8rem;
    }

    .video-card p{
      font-size:.95rem;
      color:var(--muted);
      margin:.8rem 0 0;
    }

    iframe{
      width:100%;
      aspect-ratio:16/9;
      border:none;
      border-radius:16px;
      background:#000;
    }

    .accordion{
      display:grid;
      gap:1rem;
    }

    .card{
      background:var(--panel-2);
      border:1px solid var(--border);
      border-left:6px solid var(--accent-3);
      border-radius:18px;
      padding:1.15rem 1rem;
      cursor:pointer;
      transition:.25s ease;
    }

    .card:hover{
      transform:translateY(-2px);
      box-shadow:0 12px 30px rgba(0,0,0,0.25);
      background:#23324d;
    }

    .card-title{
      display:flex;
      justify-content:space-between;
      gap:1rem;
      align-items:flex-start;
      font-weight:800;
      color:#fff;
    }

    .card-title i{
      color:var(--accent-2);
      margin-top:.15rem;
      transition:transform .2s ease;
    }

    .card.open .card-title i{
      transform:rotate(180deg);
    }

    .card-content{
      display:none;
      padding-top:.9rem;
      color:var(--muted);
    }

    .card.open .card-content{
      display:block;
    }

    .tip-tag{
      display:inline-block;
      margin-top:.75rem;
      background:rgba(99,230,226,0.12);
      color:#aaf5f2;
      padding:.3rem .65rem;
      border-radius:999px;
      font-size:.82rem;
      font-weight:700;
    }

    .quiz-wrap{
      display:grid;
      gap:1rem;
    }

    .quiz-question{
      background:var(--panel-2);
      border:1px solid var(--border);
      border-radius:16px;
      padding:1rem;
    }

    .quiz-question label{
      display:block;
      font-weight:700;
      color:#fff;
      margin-bottom:.55rem;
    }

    select, input[type="time"], input[type="number"]{
      width:100%;
      background:#0f172a;
      color:var(--text);
      border:1px solid rgba(255,255,255,0.12);
      border-radius:12px;
      padding:.85rem .9rem;
      font-size:1rem;
      outline:none;
    }

    select:focus, input:focus{
      border-color:var(--accent);
      box-shadow:0 0 0 3px rgba(99,230,226,0.12);
    }

    .result-box{
      margin-top:1.2rem;
      background:linear-gradient(135deg, rgba(31,58,46,0.8), rgba(18,50,68,0.8));
      border:1px solid rgba(99,230,226,0.18);
      border-radius:18px;
      padding:1.2rem;
    }

    .score{
      font-size:clamp(2rem,4vw,3rem);
      font-weight:900;
      color:var(--accent);
      margin-bottom:.3rem;
    }

    .gold{color:#fcd34d;font-weight:800}

    .routine-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
      gap:1rem;
      margin-top:1rem;
    }

    .habit{
      background:var(--panel-2);
      border:1px solid var(--border);
      border-radius:16px;
      padding:1rem;
    }

    .habit label{
      display:flex;
      align-items:flex-start;
      gap:.65rem;
      font-weight:700;
      color:#fff;
      margin-bottom:.8rem;
    }

    .habit input[type="checkbox"]{
      margin-top:.25rem;
      transform:scale(1.15);
      accent-color:#63e6e2;
    }

    .preview{
      background:#0f172a;
      border:1px dashed rgba(99,230,226,0.3);
      border-radius:16px;
      padding:1rem;
      margin-top:1.2rem;
      color:#dffdfd;
    }

    .preview ul{
      margin:0.7rem 0 0 1.2rem;
    }

    .preview li{
      margin:.35rem 0;
    }

    .diary-grid{
      display:grid;
      grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
      gap:1rem;
      align-items:end;
    }

    .resource-list{
      display:grid;
      gap:1rem;
      margin-top:1rem;
    }

    .resource-item{
      background:var(--panel-2);
      border:1px solid var(--border);
      border-radius:16px;
      padding:1rem;
    }

    .resource-item h3{
      color:#fff;
      margin-bottom:.35rem;
    }

    .resource-item p, .resource-item li{
      color:var(--muted);
    }

    .closing{
      text-align:center;
    }

    footer{
      margin-top:2.5rem;
      padding:2.5rem 1rem 3rem;
      background:#0a1424;
      border-top:1px solid var(--border);
      text-align:center;
      color:#cdd7ea;
    }

    footer p{
      max-width:900px;
      margin:0.5rem auto;
    }

    .small{
      font-size:.92rem;
      color:#aab8cf;
    }

    @media (max-width:700px){
      section{padding:1.4rem}
      .hero-actions{flex-direction:column;align-items:center}
      .btn{width:100%;justify-content:center}
    }
  </style>
</head>
<body>

  <header>
    <div class="hero-content container">
      <div class="eyebrow">UVic Sleep Guide • 2026</div>
      <h1>🌙 Sleep Better • Study Better</h1>
      <p class="hero-sub">
        A detailed, interactive, student-focused sleep hygiene resource for university learners. 
      </p>

      <div class="hero-actions">
        <button class="btn" onclick="document.getElementById('science').scrollIntoView({behavior:'smooth'})">
          <i class="fa-solid fa-moon"></i> Start Learning
        </button>
        <button class="btn secondary" onclick="showWelcomeMessage()">
          <i class="fa-solid fa-star"></i> What This Guide Helps With
        </button>
      </div>

      <div class="hero-grid">
        <div class="hero-stat">
          <strong>7–9 hrs</strong>
          <span>recommended for most adults and students</span>
        </div>
        <div class="hero-stat">
          <strong>23%</strong>
          <span>higher recall tied to stronger sleep-dependent memory learning</span>
        </div>
        <div class="hero-stat">
          <strong>6 videos</strong>
          <span>embedded learning tools for reinforcement</span>
        </div>
        <div class="hero-stat">
          <strong>Quiz + planner</strong>
          <span>turn information into action</span>
        </div>
      </div>
    </div>
  </header>

  <nav>
    <div class="nav-inner">
      <a href="#science">Science</a>
      <a href="#videos">Videos</a>
      <a href="#myths">Myths</a>
      <a href="#tips">Tips</a>
      <a href="#quiz">Quiz</a>
      <a href="#routine">Routine Builder</a>
      <a href="#diary">Sleep Diary</a>
      <a href="#resources">Resources</a>
      <a href="#action">Take Action</a>
    </div>
  </nav>

  <main class="container">

    <section id="science">
      <div class="section-title">
        <i class="fa-solid fa-brain"></i>
        <h2>The Science of Sleep</h2>
      </div>
      <p class="section-intro">
        Sleep is not passive downtime. It is active biological recovery, memory processing, emotional regulation, immune restoration, and cognitive preparation for the next day. For university students, that means sleep affects studying, test performance, emotional balance, concentration, motivation, and even how well new information sticks.
      </p>

      <div class="callout">
        <strong>Key idea:</strong> Repetition matters in learning, and this guide intentionally repeats the most important points in different formats: explanation, myth busting, practical advice, videos, and self-testing. That makes the resource more educational, clearer, and easier to remember.
      </div>

      <div class="grid-2">
        <div class="info-box">
          <h3>How sleep supports learning</h3>
          <p>
            During the night, the brain cycles through light sleep, deeper non-REM sleep, and REM sleep. Deep sleep supports physical restoration and immune function, while REM sleep plays a major role in memory consolidation, emotional processing, and integrating what you learned during the day.
          </p>
        </div>
        <div class="info-box">
          <h3>Why students struggle</h3>
          <p>
            University routines often disrupt healthy sleep: irregular schedules, stress, screen exposure, caffeine, assignment pressure, social commitments, and inconsistent wake times. The result is often a cycle of low energy, poor focus, late-night studying, and even worse sleep the next night.
          </p>
        </div>
        <div class="info-box">
          <h3>Circadian rhythm matters</h3>
          <p>
            Your body clock is shaped by light, activity, meals, and consistency. Morning light helps anchor wakefulness, while late-night light, especially from screens, can delay melatonin release and make falling asleep harder.
          </p>
        </div>
        <div class="info-box">
          <h3>Why “just push through” fails</h3>
          <p>
            Sleep debt does not only make you tired. It can reduce reaction time, attention, memory encoding, mood regulation, and self-control. That is why poor sleep can make studying take longer even when you are spending more time doing it.
          </p>
        </div>
      </div>

      <div class="callout">
        <strong>Most repeated lesson in this guide:</strong> better sleep does not usually come from one miracle trick. It comes from consistent habits repeated daily: regular timing, less light at night, morning light, caffeine control, a calmer wind-down, and a room that supports sleep.
      </div>
    </section>

    <section id="videos">
      <div class="section-title">
        <i class="fa-solid fa-video"></i>
        <h2>Sleep Learning Videos</h2>
      </div>
      <p class="section-intro">
        These videos reinforce the same key ideas from different angles: science, habit design, emotional health, and practical tools. That repetition makes the guide more resourceful and easier to learn from.
      </p>

      <div class="video-grid">
        <div class="video-card">
          <h3>1. Sleep Is Your Superpower – Matt Walker</h3>
          <iframe src="https://www.youtube.com/embed/5MuIMqhT8DM" title="Sleep Is Your Superpower" allowfullscreen></iframe>
          <p>A strong introduction to why sleep matters for memory, performance, and long-term health.</p>
        </div>

        <div class="video-card">
          <h3>2. Tools for Optimizing Sleep – Andrew Huberman</h3>
          <iframe src="https://www.youtube.com/embed/h2aWYjSA1Jc" title="Tools for Optimizing Sleep" allowfullscreen></iframe>
          <p>Practical science-based tools for improving sleep-wake timing and daily rhythm.</p>
        </div>

        <div class="video-card">
          <h3>3. Tips to Fall Asleep Faster – Andrew Huberman</h3>
          <iframe src="https://www.youtube.com/embed/qMjuUsizAqg" title="Tips to Fall Asleep Faster" allowfullscreen></iframe>
          <p>Useful habit-based recommendations that connect directly to student routines.</p>
        </div>

        <div class="video-card">
          <h3>4. Master Your Sleep – Andrew Huberman</h3>
          <iframe src="https://www.youtube.com/embed/lIo9FcrljDk" title="Master Your Sleep" allowfullscreen></iframe>
          <p>A broader toolkit for adults who want stronger daily alertness and night-time recovery.</p>
        </div>

        <div class="video-card">
          <h3>5. How Sleep Affects Your Emotions – Matt Walker</h3>
          <iframe src="https://www.youtube.com/embed/6F8wFkScnME" title="How Sleep Affects Your Emotions" allowfullscreen></iframe>
          <p>Important for stressed students: sleep is not only academic, it is emotional regulation too.</p>
        </div>

        <div class="video-card">
          <h3>6. Perfecting Your Sleep – Huberman + Walker</h3>
          <iframe src="https://www.youtube.com/embed/JaRGJVrJBQ8" title="Perfecting Your Sleep" allowfullscreen></iframe>
          <p>A useful deeper conversation bringing together mechanisms and practical improvements.</p>
        </div>
      </div>
    </section>

    <section id="myths">
      <div class="section-title">
        <i class="fa-solid fa-fire"></i>
        <h2>Common Myths vs Better Facts</h2>
      </div>
      <p class="section-intro">
        Click each myth to expand it. This section intentionally revisits the same core themes from a different angle: routine, recovery, caffeine, screens, naps, and the false belief that sleep can be ignored without consequences.
      </p>

      <div class="accordion">
        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 1: I can catch up on sleep fully on weekends.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Weekend recovery can help a little, but it usually does not fully undo a week of irregular sleep. You may feel slightly better, but your body clock often stays inconsistent, making Sunday night and Monday morning harder again.
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 2: All-nighters help before exams.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Staying up late may increase total study time, but it often reduces how well you learn, remember, and retrieve information. Sleep supports memory consolidation, so cutting sleep can weaken the value of the studying you just did.
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 3: Caffeine fixes tiredness.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Caffeine can temporarily increase alertness, but it does not replace lost sleep. It may also linger in the body for hours and interfere with deep sleep later, especially when used late in the day.
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 4: Screens before bed do not matter if I am already tired.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Bright screen light can delay melatonin release and keep the brain mentally activated. Even when you feel sleepy, screen use can increase sleep latency and make the quality of sleep worse.
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 5: Naps always repair poor night sleep.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Short naps can help some people, but long or late naps may reduce sleep pressure and make it harder to fall asleep at night. Naps should support, not replace, healthy night-time sleep.
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 6: Alcohol helps me sleep better.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Alcohol may make you feel sleepy faster, but it often fragments sleep and reduces sleep quality later in the night, especially REM-rich sleep.
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 7: I function perfectly on 5 hours every night.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Many people feel adapted to chronic short sleep, but performance, mood, patience, reaction time, and memory can still decline. Feeling “used to it” is not the same as functioning at your best.
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>Myth 8: Sleep only matters for physical energy.</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Sleep also affects mental clarity, emotional control, learning, immunity, stress response, motivation, and decision-making. For students, it shapes both academic and personal wellbeing.
          </div>
        </div>
      </div>
    </section>

    <section id="tips">
      <div class="section-title">
        <i class="fa-solid fa-lightbulb"></i>
        <h2>12 Clear, Repeated, Evidence-Based Sleep Tips</h2>
      </div>
      <p class="section-intro">
        These tips repeat the major lessons of the guide in practical language. Repetition here is intentional: you learn the science, then the myths, and now the daily habits that actually make change possible.
      </p>

      <div class="accordion">
        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>1. Keep a consistent bedtime and wake time</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Going to bed and waking up at roughly the same time every day helps stabilize circadian rhythm. This is one of the most useful habits in the entire guide because it improves both falling asleep and morning alertness.
            <div class="tip-tag">Most important habit</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>2. Reduce screens before bed</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            A screen curfew helps lower light exposure and mental stimulation. Even 30 to 60 minutes away from intense screen use can support a smoother transition into sleep.
            <div class="tip-tag">Light management</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>3. Keep the room cool, dark, and quiet</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Environment matters. A cooler room, less noise, and reduced light can make sleep more continuous and less fragmented.
            <div class="tip-tag">Bedroom setup</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>4. Get morning daylight exposure</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Early light tells your body that the day has started. This helps anchor your rhythm and often improves night-time sleepiness later.
            <div class="tip-tag">Circadian anchor</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>5. Avoid caffeine too late in the day</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Caffeine can remain active longer than expected. If falling asleep is difficult, reducing afternoon or evening caffeine is one of the clearest adjustments to test.
            <div class="tip-tag">Energy timing</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>6. Build a short wind-down routine</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            A repeated pre-sleep routine helps your brain shift from performance mode to recovery mode. Stretching, journaling, dim lights, reading, and calm music are examples.
            <div class="tip-tag">Behavior cue</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>7. Use the bed mainly for sleep</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            If the bed becomes a place for studying, scrolling, stressing, and watching videos, the brain stops associating it mainly with rest.
            <div class="tip-tag">Sleep association</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>8. Exercise regularly, but time it well</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Movement supports sleep quality, but very intense late-night exercise can keep some people too activated close to bedtime.
            <div class="tip-tag">Recovery balance</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>9. Keep naps short and earlier in the day</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Short naps can refresh attention, but long or late naps may reduce sleep drive at night.
            <div class="tip-tag">Nap control</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>10. If you cannot sleep, reset gently</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            If you are lying awake for a long time, getting up briefly for a calm, low-light activity can be better than staying in bed frustrated.
            <div class="tip-tag">CBT-I inspired</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>11. Track patterns, not perfection</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Tracking helps you notice what affects your sleep: stress, caffeine, naps, workload, screen time, or wake time consistency.
            <div class="tip-tag">Self-awareness</div>
          </div>
        </div>

        <div class="card" onclick="toggleCard(this)">
          <div class="card-title">
            <span>12. Improve one habit first, then build</span>
            <i class="fa-solid fa-chevron-down"></i>
          </div>
          <div class="card-content">
            Sustainable change is usually gradual. Start with the habit that gives the biggest benefit for you, such as wake time consistency or screen reduction.
            <div class="tip-tag">Behavior change</div>
          </div>
        </div>
      </div>
    </section>

    <section id="quiz">
      <div class="section-title">
        <i class="fa-solid fa-list-check"></i>
        <h2>Sleep Hygiene Self-Quiz</h2>
      </div>
      <p class="section-intro">
        Answer honestly. This quiz repeats the guide’s main habits in question form, which helps reinforce the learning while giving you personalized feedback.
      </p>

      <div class="quiz-wrap">
        <div class="quiz-question">
          <label for="q1">1. How consistent is your bedtime and wake time?</label>
          <select id="q1">
            <option value="0">Rarely consistent</option>
            <option value="2">Sometimes consistent</option>
            <option value="4">Usually consistent</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q2">2. Do you avoid screens 30–60 minutes before bed?</label>
          <select id="q2">
            <option value="0">Rarely</option>
            <option value="2">Sometimes</option>
            <option value="4">Usually</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q3">3. Is your room cool, dark, and reasonably quiet?</label>
          <select id="q3">
            <option value="0">Not really</option>
            <option value="2">Partly</option>
            <option value="4">Yes, most nights</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q4">4. Do you get regular daytime movement or exercise?</label>
          <select id="q4">
            <option value="0">Rarely</option>
            <option value="2">Sometimes</option>
            <option value="4">Usually</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q5">5. Do you avoid caffeine later in the day?</label>
          <select id="q5">
            <option value="0">Rarely</option>
            <option value="2">Sometimes</option>
            <option value="4">Usually</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q6">6. Do you feel reasonably rested after waking?</label>
          <select id="q6">
            <option value="0">Rarely</option>
            <option value="2">Sometimes</option>
            <option value="4">Usually</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q7">7. Do you have any wind-down routine at night?</label>
          <select id="q7">
            <option value="0">No</option>
            <option value="2">Sometimes</option>
            <option value="4">Yes, usually</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q8">8. Do you get morning daylight exposure?</label>
          <select id="q8">
            <option value="0">Rarely</option>
            <option value="2">Sometimes</option>
            <option value="4">Usually</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q9">9. Do you mainly use your bed for sleep rather than work or scrolling?</label>
          <select id="q9">
            <option value="0">Rarely</option>
            <option value="2">Sometimes</option>
            <option value="4">Usually</option>
          </select>
        </div>

        <div class="quiz-question">
          <label for="q10">10. Do you notice and track your sleep patterns?</label>
          <select id="q10">
            <option value="0">Rarely</option>
            <option value="2">Sometimes</option>
            <option value="4">Usually</option>
          </select>
        </div>
      </div>

      <div style="margin-top:1rem;display:flex;gap:1rem;flex-wrap:wrap;">
        <button class="btn" onclick="calculateScore()">
          <i class="fa-solid fa-chart-column"></i> Submit Quiz
        </button>
        <button class="btn secondary" onclick="quickQuiz()">
          <i class="fa-solid fa-bolt"></i> Quick Sleep Fact
        </button>
      </div>

      <div id="quiz-result" class="result-box" style="display:none;"></div>
    </section>

    <section id="routine">
      <div class="section-title">
        <i class="fa-solid fa-calendar-check"></i>
        <h2>Build Your Personal Sleep Routine</h2>
      </div>
      <p class="section-intro">
        Select habits you want to follow tonight. This section turns repeated advice into an action plan. The more specific the plan, the easier it is to follow.
      </p>

      <div class="routine-grid">
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="No screens before bed"> No screens before bed</label>
          <input type="time" id="t1" value="22:00">
        </div>
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="Consistent bedtime"> Consistent bedtime</label>
          <input type="time" id="t2" value="23:00">
        </div>
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="Cool, dark room setup"> Cool, dark room setup</label>
          <input type="time" id="t3" value="22:40">
        </div>
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="10-minute wind-down stretch"> 10-minute wind-down stretch</label>
          <input type="time" id="t4" value="22:30">
        </div>
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="Morning daylight walk"> Morning daylight walk</label>
          <input type="time" id="t5" value="08:00">
        </div>
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="No caffeine after 2 pm"> No caffeine after 2 pm</label>
          <input type="time" id="t6" value="14:00">
        </div>
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="Bed for sleep only"> Bed for sleep only</label>
          <input type="time" id="t7" value="23:00">
        </div>
        <div class="habit">
          <label><input type="checkbox" class="habit-check" data-label="Gratitude or reflection journal"> Gratitude or reflection journal</label>
          <input type="time" id="t8" value="22:45">
        </div>
      </div>

      <div style="margin-top:1rem;display:flex;gap:1rem;flex-wrap:wrap;">
        <button class="btn" onclick="updateRoutine()">
          <i class="fa-solid fa-wand-magic-sparkles"></i> Build Routine
        </button>
        <button class="btn secondary" onclick="saveRoutineMessage()">
          <i class="fa-solid fa-file-export"></i> Save / Export Plan
        </button>
      </div>

      <div id="routine-output" class="preview">
        Your routine preview appears here. Select some habits and click <strong>Build Routine</strong>.
      </div>
    </section>

    <section id="diary">
      <div class="section-title">
        <i class="fa-solid fa-chart-line"></i>
        <h2>Sleep Diary Simulator</h2>
      </div>
      <p class="section-intro">
        Logging one night will not solve everything, but tracking patterns helps you learn what affects your sleep and reinforces the guide’s main message: awareness + consistency = better outcomes.
      </p>

      <div class="diary-grid">
        <div>
          <label for="hours">Hours slept last night</label>
          <input type="number" id="hours" min="0" max="14" step="0.5" value="6">
        </div>
        <div>
          <label for="rested">How rested do you feel? (1–10)</label>
          <input type="number" id="rested" min="1" max="10" step="1" value="4">
        </div>
      </div>

      <div style="margin-top:1rem;display:flex;gap:1rem;flex-wrap:wrap;">
        <button class="btn" onclick="logDiary()">
          <i class="fa-solid fa-pen"></i> Log Night
        </button>
      </div>

      <div id="diary-output" class="result-box" style="margin-top:1rem;">
        Log one night to see a simple interpretation and a simulated improvement message.
      </div>
    </section>

    <section id="resources">
      <div class="section-title">
        <i class="fa-solid fa-life-ring"></i>
        <h2>UVic, Victoria, and General Support Resources</h2>
      </div>
      <p class="section-intro">
        Good educational resources should not only explain the problem. They should also direct people toward support, next steps, and local options.
      </p>

      <div class="resource-list">
        <div class="resource-item">
          <h3>UVic Student Wellness</h3>
          <p>Explore campus wellness services, counselling supports, stress management resources, and student health education. This guide works best when paired with real support if sleep problems are persistent.</p>
        </div>
        <div class="resource-item">
          <h3>Primary care and referrals</h3>
          <p>If sleep difficulty is ongoing, severe, or affecting mental health, academics, safety, or daily functioning, speak with a doctor or nurse practitioner. Sleep clinics or specialist referrals may help.</p>
        </div>
        <div class="resource-item">
          <h3>Campus habits that can help right away</h3>
          <ul>
            <li>Get morning daylight when possible</li>
            <li>Reduce late-night screen intensity</li>
            <li>Create a calmer sleep space</li>
            <li>Use roommates or friends as accountability partners</li>
            <li>Track patterns for at least one week</li>
          </ul>
        </div>
        <div class="resource-item">
          <h3>When to seek help sooner</h3>
          <p>Seek support sooner if you are experiencing persistent insomnia, extreme daytime sleepiness, loud snoring with choking or gasping, major mood disruption, or inability to function during the day.</p>
        </div>
      </div>
    </section>

    <section id="action" class="closing">
      <div class="section-title" style="justify-content:center;">
        <i class="fa-solid fa-rocket"></i>
        <h2>Take Action Tonight</h2>
      </div>
      <p class="section-intro" style="max-width:850px;margin:0 auto 1.2rem;">
        The biggest educational message of this whole guide is simple and worth repeating clearly: better sleep usually comes from repeated small habits, not one dramatic fix. Choose one or two habits tonight, repeat them tomorrow, and build from there.
      </p>
      <div class="callout" style="text-align:left;max-width:900px;margin:0 auto 1.4rem;">
        <strong>Start with this simple plan:</strong><br>
        1. Set tomorrow’s wake-up time.<br>
        2. Stop screens a little earlier.<br>
        3. Keep caffeine earlier in the day.<br>
        4. Get light in the morning.<br>
        5. Repeat the same pattern for several days before judging whether it is working.
      </div>
      <button class="btn" onclick="shareMessage()">
        <i class="fa-solid fa-share-nodes"></i> Share This Resource
      </button>
    </section>

  </main>

  <footer>
    <p><strong>Sleep Better • Study Better </strong>  - written and designed single-page educational resource by Knox.</p>
    <p class="small">
      The semi-polished version 
    </p>
    <p class="small">
      Do Better! Be Better!
    </p>
  </footer>

  <script>
    function showWelcomeMessage() {
      alert("This guide helps students understand sleep science, break common myths, build routines, self-assess habits, and find support. The repetition is intentional so the ideas are easier to learn and apply.");
    }

    function toggleCard(card) {
      card.classList.toggle('open');
    }

    function quickQuiz() {
      document.getElementById('quiz-result').style.display = 'block';
      document.getElementById('quiz-result').innerHTML = `
        <p class="score">Quick Sleep Fact</p>
        <p><span class="gold">Key takeaway:</span> better sleep supports memory, focus, mood, and recovery. The most repeated recommendation in this guide is consistency: regular sleep and wake times are one of the strongest foundations for improvement.</p>
      `;
    }

    function calculateScore() {
      let score = 0;
      for (let i = 1; i <= 10; i++) {
        score += parseInt(document.getElementById('q' + i).value) || 0;
      }

      let message = '';
      let advice = '';

      if (score >= 32) {
        message = 'Excellent foundation. Your current habits already support strong sleep hygiene.';
        advice = 'Keep reinforcing consistency, protect your evening wind-down, and maintain morning light exposure so your routine stays strong even during busy academic weeks.';
      } else if (score >= 20) {
        message = 'Good start. You have useful habits in place, but there is room to tighten the routine.';
        advice = 'Your highest-value upgrades are likely bedtime consistency, reducing late screens, and being more intentional with caffeine timing.';
      } else {
        message = 'There is clear room for improvement, which also means there is strong potential for progress.';
        advice = 'Start with only one or two changes: a more regular wake time and less screen use before bed. Build from there rather than trying to fix everything at once.';
      }

      document.getElementById('quiz-result').innerHTML = `
        <p class="score">Your Sleep Score: ${score} / 40</p>
        <p><strong>${message}</strong></p>
        <p>${advice}</p>
        <p class="small">Reminder: this score is educational, not diagnostic. It is a habit snapshot to help guide self-reflection and planning.</p>
      `;
      document.getElementById('quiz-result').style.display = 'block';
    }

    function updateRoutine() {
      const checks = document.querySelectorAll('.habit-check');
      const selected = [];

      checks.forEach((check, index) => {
        if (check.checked) {
          const timeInput = document.getElementById('t' + (index + 1));
          const label = check.dataset.label;
          selected.push({ label, time: timeInput ? timeInput.value : '' });
        }
      });

      if (!selected.length) {
        document.getElementById('routine-output').innerHTML =
          'You have not selected any habits yet. Start with one or two high-impact habits like a consistent bedtime or reducing screens before bed.';
        return;
      }

      let tips = `
        <strong>Your routine tonight:</strong>
        <ul>
          ${selected.map(item => `<li><strong>${item.time}</strong> — ${item.label}</li>`).join('')}
        </ul>
        <p style="margin-top:.9rem;"><strong>Why this matters:</strong> a routine works best when it is specific, repeatable, and realistic. Repeating a few habits consistently is usually better than creating a perfect plan you cannot maintain.</p>
      `;

      document.getElementById('routine-output').innerHTML = tips;
    }

    function saveRoutineMessage() {
      alert("Routine saved conceptually. In a final submission version, this could export to PDF or save to local storage with your name, date, and selected habits.");
    }

    function logDiary() {
      const hours = parseFloat(document.getElementById('hours').value) || 0;
      const rested = parseInt(document.getElementById('rested').value) || 0;

      let interpretation = '';
      let nextStep = '';

      if (hours >= 7 && rested >= 7) {
        interpretation = 'This looks like a relatively strong sleep night.';
        nextStep = 'Focus on repeating the same pattern so that good sleep becomes more consistent rather than occasional.';
      } else if (hours >= 6) {
        interpretation = 'This was a moderate night: not terrible, but probably leaving some recovery and focus on the table.';
        nextStep = 'Try improving one evening habit tonight, especially screen timing, caffeine timing, or bedtime consistency.';
      } else {
        interpretation = 'This was a short sleep night and may affect focus, mood, and efficiency today.';
        nextStep = 'Protect your next sleep opportunity. Avoid using tiredness as a reason to overuse caffeine late in the day, because that can continue the cycle.';
      }

      const simulated = Math.min(hours + 1.5, 9).toFixed(1);

      document.getElementById('diary-output').innerHTML = `
        <p><strong>Logged:</strong> ${hours} hours slept, rested rating ${rested}/10.</p>
        <p><strong>Interpretation:</strong> ${interpretation}</p>
        <p><strong>Suggested next step:</strong> ${nextStep}</p>
        <p><strong>Simulated improvement message:</strong> if you consistently apply a few strong habits, your average could move toward about ${simulated} hours over time.</p>
        <p class="small">This is an educational simulation, not a medical prediction.</p>
      `;
    }

    function shareMessage() {
      alert("Thanks for sharing this resource. Repetition, clarity, and practical action are what make sleep education actually useful.");
    }
  </script>
</body>
</html>

