<script>

/* THEME */

function toggleMode(){

document.body.classList.toggle('light-mode');

}

/* AGE MODAL */

function openModal(){

document.getElementById('ageModal')
.style.display='flex';

}

function closeModal(){

document.getElementById('ageModal')
.style.display='none';

}

/* CASE DATABASE */

const cases = {

"vova and vika stepsiblings":"vova-vika.html",

"samantha rupnow":"samantha-rupnow.html",

"rina palenkova":"rina-palenkova.html",

"vladislav roslyakov":"vladislav-roslyakov.html",

"pekka":"pekka.html",

"brenton":"brenton.html",

"payton":"payton.html",

"adam lanza":"adam-lanza.html",

"arthur achleithner":"arthur-achleithner.html"

};

/* SEARCH FUNCTION */

function searchCase(){

const input =
document
.getElementById('searchInput')
.value
.toLowerCase()
.trim();

if(cases[input]){

window.location.href = cases[input];

}else{

alert("Case not found.");

}

}

/* ENTER KEY SUPPORT */

document
.getElementById("searchInput")
.addEventListener("keypress", function(e){

if(e.key === "Enter"){

searchCase();

}

});

</script>
