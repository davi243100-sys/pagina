<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Blox Mundial – Loja de Contas</title>
<style>
body {
    font-family: Arial, sans-serif;
    background:#f2f2f2;
    padding:20px;
}
h2 { margin-bottom:20px; }
.product {
    background:#fff;
    border-radius:12px;
    padding:15px;
    margin-bottom:20px;
    border:1px solid #ccc;
}
.small { font-size:13px; color:#555; }
.price { font-weight:bold; margin-top:5px; }

button {
    width:100%;
    padding:10px;
    margin-top:12px;
    border:none;
    border-radius:8px;
    background:#4CAF50;
    color:white;
    font-size:15px;
    cursor:pointer;
}

button.disabled {
    background:#999;
    cursor:not-allowed;
}

.warning {
    background:#ffe5e5;
    color:#b30000;
    padding:8px;
    border-radius:8px;
    font-size:13px;
    margin-bottom:10px;
}
img {
    display:block;
    margin:15px auto;
    max-width:220px;
}
#entrega {
    display:none;
    position:fixed;
    inset:0;
    background:rgba(0,0,0,.6);
    justify-content:center;
    align-items:center;
}
#box {
    background:#fff;
    padding:20px;
    border-radius:10px;
    width:90%;
    max-width:320px;
}
input {
    width:100%;
    padding:8px;
    margin-bottom:8px;
}
</style>
</head>
<body>

<h2>Contas Blox Fruits</h2>

<!-- CONTA SHARK ANCHOR / KITSUNE (INDISPONÍVEL) -->
<div class="product">
    <div class="warning">
        ⚠ Conta teste / não funciona<br>
        Conta já tem dono<br>
        Conta é do dono da loja
    </div>

    <strong>Shark Anchor + Kitsune</strong>
    <div class="small">Nível 2800</div>
    <div class="price">INDISPONÍVEL</div>

    <img src="https://i.imgur.com/1QeQZ4t.png">

    <button class="disabled" disabled>Indisponível</button>
</div>

<!-- CONTA BUDDHA -->
<div class="product">
    <strong>Buddha + CDK</strong>
    <div class="small">Nível 2800</div>
    <div class="price">R$ 19,90</div>

    <!-- IMAGEM QUE VOCÊ MANDOU -->
    <img src="imagem-buddha.png" alt="Buddha">

    <button onclick="abrirEntrega('AlbertGrimes259','secret244')">
        Comprar
    </button>
</div>

<!-- ENTREGA -->
<div id="entrega">
    <div id="box">
        <h3>Dados da Conta</h3>

        <label>Usuário</label>
        <input id="user" readonly>
        <button onclick="copiar('user')">Copiar Usuário</button>

        <label>Senha</label>
        <input id="pass" readonly>
        <button onclick="copiar('pass')">Copiar Senha</button>

        <button onclick="fechar()" style="background:#d9534f;margin-top:10px;">
            Fechar
        </button>
    </div>
</div>

<script>
function abrirEntrega(u,p){
    document.getElementById("user").value=u;
    document.getElementById("pass").value=p;
    document.getElementById("entrega").style.display="flex";
}
function fechar(){
    document.getElementById("entrega").style.display="none";
}
function copiar(id){
    let el=document.getElementById(id);
    el.select();
    document.execCommand("copy");
}
</script>

</body>
</html>
