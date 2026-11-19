# portal-operacional-reyes<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">

<title>Portal Operacional Reyes</title>

<style>
*{
    margin:0;
    padding:0;
    box-sizing:border-box;
    font-family:Arial,sans-serif;
}

body{
    background:#f4f6f9;
}

.header{
    background:#1f2937;
    color:white;
    padding:20px;
}

.container{
    max-width:1200px;
    margin:auto;
    padding:20px;
}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(220px,1fr));
    gap:20px;
}

.card{
    background:white;
    padding:20px;
    border-radius:12px;
    box-shadow:0 2px 8px rgba(0,0,0,.1);
}

.numero{
    font-size:32px;
    font-weight:bold;
    color:#2563eb;
}

.formulario{
    margin-top:25px;
}

input{
    width:100%;
    margin-bottom:10px;
    padding:12px;
    border:1px solid #ddd;
    border-radius:8px;
}

button{
    background:#2563eb;
    color:white;
    border:none;
    padding:12px;
    width:100%;
    border-radius:8px;
    cursor:pointer;
}

button:hover{
    background:#1d4ed8;
}

.lista{
    margin-top:20px;
}

.item{
    background:white;
    padding:12px;
    margin-top:10px;
    border-radius:8px;
}
</style>
</head>

<body>

<div class="header">
    <h1>Portal Operacional Reyes</h1>
</div>

<div class="container">

<div class="grid">

<div class="card">
    <h3>Processos Ativos</h3>
    <div class="numero">23</div>
</div>

<div class="card">
    <h3>Aguardando Cliente</h3>
    <div class="numero">8</div>
</div>

<div class="card">
    <h3>Concluídos Hoje</h3>
    <div class="numero">15</div>
</div>

<div class="card">
    <h3>Atrasados</h3>
    <div class="numero">3</div>
</div>

</div>

<div class="card formulario">

<h2>Novo Processo</h2>

<input id="nome" placeholder="Nome">
<input id="cpf" placeholder="CPF">

<button onclick="adicionar()">
Adicionar Processo
</button>

<div id="lista" class="lista"></div>

</div>

</div>

<script>

function adicionar(){

const nome =
document.getElementById("nome").value;

const cpf =
document.getElementById("cpf").value;

if(!nome || !cpf){
alert("Preencha Nome e CPF");
return;
}

const div =
document.createElement("div");

div.className = "item";

div.innerHTML =
"<strong>" + nome +
"</strong><br>CPF: " + cpf +
"<br>Status: Novo";

document
.getElementById("lista")
.appendChild(div);

document.getElementById("nome").value="";
document.getElementById("cpf").value="";
}

</script>

</body>
</html>
