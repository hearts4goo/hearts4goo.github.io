Replace everything inside your `index.html` with this code.
It matches the mascot style more and includes:

* dark/light mode toggle
* pink aesthetic
* mascot section
* animated buttons
* responsive layout
* fandom/community vibe

Before using it:

1. upload your mascot image into the repo
2. name it:

```html id="a1x92m"
mascot.png
```

Then paste this into `index.html`:

```html id="k92xla"
<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Kotjas Archive</title>

<link href="https://fonts.googleapis.com/css2?family=Special+Elite&family=Quicksand:wght@400;600&display=swap" rel="stylesheet">

<style>

:root{
--bg:#0d0b10;
--card:#17131d;
--text:#ffeef5;
--pink:#ff8db4;
--border:#3b2d38;
--accent:#ff5d94;
}

.light-mode{
--bg:#fff4f8;
--card:#ffe5ee;
--text:#2d1b25;
--pink:#d85b87;
--border:#f2bdd1;
--accent:#b80052;
}

*{
margin:0;
padding:0;
box-sizing:border-box;
}

body{
background:var(--bg);
color:var(--text);
font-family:'Quicksand',sans-serif;
transition:0.3s;
overflow-x:hidden;
}

header{
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 40px;
border-bottom:1px solid var(--border);
background:rgba(0,0,0,0.2);
backdrop-filter:blur(10px);
position:sticky;
top:0;
z-index:100;
}

.logo{
font-size:32px;
font-family:'Special Elite',cursive;
color:var(--pink);
}

nav{
display:flex;
gap:25px;
align-items:center;
}

nav a{
text-decoration:none;
color:var(--text);
font-size:15px;
transition:0.2s;
}

nav a:hover{
color:var(--pink);
}

.toggle-btn{
background:var(--card);
border:1px solid var(--border);
padding:10px 16px;
border-radius:12px;
color:var(--text);
cursor:pointer;
}

.hero{
display:grid;
grid-template-columns:1fr 1fr;
align-items:center;
padding:70px 10%;
gap:40px;
min-height:85vh;
}

.hero-text h1{
font-size:70px;
line-height:1;
font-family:'Special Elite',cursive;
margin-bottom:20px;
}

.hero-text h1 span{
color:var(--pink);
}

.hero-text p{
font-size:18px;
line-height:1.8;
max-width:600px;
opacity:0.9;
margin-bottom:30px;
}

.buttons{
display:flex;
gap:20px;
flex-wrap:wrap;
}

.btn{
padding:14px 28px;
border-radius:14px;
text-decoration:none;
font-weight:bold;
transition:0.25s;
}

.primary{
background:var(--pink);
color:black;
}

.primary:hover{
transform:translateY(-3px);
}

.secondary{
border:1px solid var(--border);
color:var(--text);
background:var(--card);
}

.secondary:hover{
border-color:var(--pink);
}

.mascot{
display:flex;
justify-content:center;
align-items:center;
}

.mascot img{
width:100%;
max-width:420px;
image-rendering:pixelated;
filter:drop-shadow(0 0 25px rgba(255,141,180,0.3));
animation:float 4s ease-in-out infinite;
}

@keyframes float{
0%{transform:translateY(0px);}
50%{transform:translateY(-10px);}
100%{transform:translateY(0px);}
}

.section{
padding:80px 10%;
}

.section-title{
font-size:40px;
margin-bottom:40px;
font-family:'Special Elite',cursive;
color:var(--pink);
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(260px,1fr));
gap:25px;
}

.card{
background:var(--card);
border:1px solid var(--border);
padding:25px;
border-radius:20px;
transition:0.25s;
}

.card:hover{
transform:translateY(-5px);
border-color:var(--pink);
}

.card h3{
margin-bottom:15px;
color:var(--pink);
}

.card p{
line-height:1.7;
opacity:0.9;
}

footer{
padding:40px;
text-align:center;
border-top:1px solid var(--border);
margin-top:40px;
opacity:0.7;
}

@media(max-width:900px){

.hero{
grid-template-columns:1fr;
text-align:center;
}

.hero-text h1{
font-size:52px;
}

.buttons{
justify-content:center;
}

nav{
display:none;
}

}

</style>
</head>

<body>

<header>

<div class="logo">
KOTJAS ARCHIVE
</div>

<nav>
<a href="#">Home</a>
<a href="#">Cases</a>
<a href="#">Missing</a>
<a href="#">Timeline</a>
<a href="#">Community</a>
</nav>

<button class="toggle-btn" onclick="toggleMode()">
Toggle Theme
</button>

</header>

<section class="hero">

<div class="hero-text">

<h1>
truth.<br>
awareness.<br>
<span>change.</span>
</h1>

<p>
Kotjas Archive documents crimes, disappearances,
and tragedies for awareness and education.
A place for research, discussion, timelines,
and community remembrance.
</p>

<div class="buttons">

<a href="#" class="btn primary">
Explore Cases
</a>

<a href="#" class="btn secondary">
Join Community
</a>

</div>

</div>

<div class="mascot">
<img src="mascot.png" alt="Mascot">
</div>

</section>

<section class="section">

<h2 class="section-title">
Recent Cases
</h2>

<div class="cards">

<div class="card">
<h3>City Mall Shooting</h3>
<p>
Archive documenting the timeline,
investigation, and aftermath.
</p>
</div>

<div class="card">
<h3>Riverside Disappearance</h3>
<p>
Case files, witness statements,
and community discussion.
</p>
</div>

<div class="card">
<h3>Oakwood Murders</h3>
<p>
Historical archive preserving
details and timelines.
</p>
</div>

</div>

</section>

<footer>
Kotjas Archive • awareness project
</footer>

<script>

function toggleMode(){
document.body.classList.toggle("light-mode");
}

</script>

</body>
</html>
```
