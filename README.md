<!DOCTYPE html>

<html lang="pt-br">

<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Asphalt Wolves | Recrutamento</title>

<style>

body{
margin:0;
font-family:Arial, Helvetica, sans-serif;
background:linear-gradient(135deg,#0a1d40,#133c8b);
display:flex;
align-items:center;
justify-content:center;
min-height:100vh;
color:white;
}

.card{
background:rgba(0,0,0,0.45);
padding:40px;
border-radius:20px;
width:90%;
max-width:520px;
box-shadow:0 10px 35px rgba(0,0,0,0.4);
backdrop-filter:blur(8px);
}

.logo{
text-align:center;
margin-bottom:15px;
}

.logo img{
width:130px;
}

h3{
margin:5px 0;
text-align:center;
font-size:22px;
}

.sub{
text-align:center;
font-size:14px;
opacity:0.8;
margin-bottom:25px;
}

label{
display:block;
margin-top:14px;
font-size:14px;
}

input, textarea{
width:100%;
padding:10px;
margin-top:6px;
border-radius:8px;
border:none;
outline:none;
background:#163a7a;
color:white;
}

textarea{
resize:none;
}

.grid{
display:grid;
grid-template-columns:1fr 1fr;
gap:10px;
}

.small{
font-size:12px;
opacity:0.7;
}

button{
margin-top:20px;
width:100%;
padding:12px;
border:none;
border-radius:8px;
background:#2f7bff;
color:white;
font-size:15px;
cursor:pointer;
transition:0.2s;
}

button:hover{
background:#1b57c9;
}

.success{
display:none;
text-align:center;
}

.success h2{
color:#7cffc1;
}

</style>

</head>

<body>

<div class="card">

<div class="logo">
<img src="logo.png">
</div>

<div id="formArea">

<h3>Entrar para a Asphalt Wolves</h3>
<p class="sub">Preencha os dados abaixo para se candidatar.</p>

<form id="recruitForm">

<label>Gamertag / Nome no jogo *</label> <input type="text" id="gamertag" maxlength="50" required placeholder="Seu nome no jogo">

<div class="grid">

<div>
<label>Sua idade *</label>
<input type="number" id="age" min="15" max="99" required placeholder="Ex: 18">
<p class="small">Mínimo 15 anos</p>
</div>

<div>
<label>Horas jogadas *</label>
<input type="number" id="hours" min="10" required placeholder="Ex: 50">
<p class="small">Mínimo 10 horas</p>
</div>

</div>

<label>Instagram (opcional)</label> <input type="text" id="instagram" maxlength="100" placeholder="@seuinstagram">

<label>Por que quer entrar na Wolves? *</label>

<textarea id="why" rows="4" maxlength="500" required placeholder="Conte um pouco sobre você e por que quer fazer parte da equipe..."></textarea>

<button type="submit">Enviar candidatura</button>

</form>

</div>

<div class="success" id="success">

<h2>✔ Candidatura enviada!</h2>

<p>
A alcateia recebeu seu pedido.<br>
Vamos analisar e entrar em contato em breve.
</p>

</div>

</div>

<script>

document.getElementById("recruitForm").addEventListener("submit", function(e){

e.preventDefault()

let gamertag = document.getElementById("gamertag").value
let age = parseInt(document.getElementById("age").value)
let hours = parseInt(document.getElementById("hours").value)
let insta = document.getElementById("instagram").value
let why = document.getElementById("why").value

if(isNaN(age) || age < 15){
alert("Você precisa ter pelo menos 15 anos para se candidatar.")
return
}

if(isNaN(hours) || hours < 10){
alert("Você precisa ter pelo menos 10 horas registradas.")
return
}

document.getElementById("formArea").style.display="none"
document.getElementById("success").style.display="block"

})

</script>

</body>
</html>
