<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Loja Blox Fruits</title>
<style>
    body {
        font-family: Arial;
        background:#f5f5f5;
        padding:20px;
    }
    h2 { margin-top:30px; }
    .section {
        background:white;
        padding:18px;
        border-radius:12px;
        border:1px solid #ddd;
        margin-bottom:25px;
    }
    .product {
        margin-bottom:18px;
        padding:12px;
        border:1px solid #ddd;
        border-radius:10px;
        background:#fff;
    }
    .small {
        font-size:13px;
        opacity:.8;
    }
    button {
        background:#4CAF50;
        color:white;
        width:100%;
        padding:10px;
        border:none;
        border-radius:8px;
        cursor:pointer;
        font-weight:bold;
    }
</style>
</head>
<body>

<!-- ========================= -->
<!--        PRODUTOS           -->
<!-- ========================= -->
<section class="section">
<h2>Produtos em destaque</h2>

<!-- Buddha FREE -->
<div class="product">
    <div style="display:flex; justify-content:space-between; align-items:center;">
        <strong>Buddha – Level 0</strong>
        <span class="small" style="color:green; font-weight:bold;">R$ 0,00 (FREE)</span>
    </div>
    <div class="small" style="margin-top:6px;">
        Conta básica com fruta Buddha. Ideal para iniciantes — entrega imediata.
    </div>
    <div style="margin-top:10px;">
        <button onclick="abrirEntrega('ClarenceMcintyre4402','valeria2')">PEGAR GRÁTIS</button>
    </div>
</div>

<!-- Conta Buddha + CDK + Lv. 2800 -->
<div class="product">
    <div style="display:flex; justify-content:space-between; align-items:center;">
        <strong>Conta Buddha + CDK + Lv. 2800</strong>
        <span class="small">R$ 40</span>
    </div>
    <div class="small">Conta completa, forte e pronta para endgame.</div>
    <div style="margin-top:10px;">
        <button onclick="pagar(40, 'AlbertGrimes259','secret244')">COMPRAR</button>
    </div>
</div>

<!-- Guia Premium -->
<div class="product">
    <div style="display:flex; justify-content:space-between; align-items:center;">
        <strong>Guia Premium</strong>
        <span class="small">R$ 12</span>
    </div>
    <div class="small">E-book com estratégias de Blox Fruits.</div>
</div>

<!-- Pacote VIP -->
<div class="product">
    <div style="display:flex; justify-content:space-between; align-items:center;">
        <strong>Pacote VIP</strong>
        <span class="small">R$ 60</span>
    </div>
    <div class="small">Combo de serviços com desconto e prioridade.</div>
</div>

</section>

<!-- ========================= -->
<!--          PIX              -->
<!-- ========================= -->
<section class="section">
<h2>Pagamento via PIX</h2>

<p>Escaneie o QR Code para pagar:</p>

<img src="https://i.imgur.com/1QeQZ4t.png" style="width:200px; border-radius:10px;">

<p style="margin-top:10px;"><strong>Código copia e cola:</strong></p>

<textarea style="width:100%; height:80px;">00020126360014BR.GOV.BCB.PIX0114+5555999231517520400005303986540521.005802BR5925David Luiz Turani Bechene6009SAO PAULO62140510nWJgB4hhTi63042A0A</textarea>

</section>

<!-- ========================= -->
<!--  JANELA DE ENTREGA       -->
<!-- ========================= -->
<div id="entrega" style="
    display:none; 
    position:fixed; 
    top:0; left:0; width:100%; height:100%;
    background:rgba(0,0,0,0.6); 
    justify-content:center; 
    align-items:center;
">
    <div style="background:white; padding:25px; border-radius:12px; width:320px;">
        <h3>Dados da Conta</h3>

        <p><strong>Usuário:</strong></p>
        <input id="userBox" style="width:100%; padding:8px; margin-bottom:10px;" readonly>
        <button onclick="copiar('userBox')">Copiar Usuário</button>

        <p style="margin-top:15px;"><strong>Senha:</strong></p>
        <input id="passBox" style="width:100%; padding:8px;" readonly>
        <button onclick="copiar('passBox')">Copiar Senha</button>

        <button style="background:#e53935; margin-top:18px;" onclick="fecharEntrega()">Fechar</button>
    </div>
</div>

<script>
function pagar(valor, user, pass) {
    alert("Após pagar R$ " + valor + " via PIX, os dados irão abrir.");
    abrirEntrega(user, pass);
}

function abrirEntrega(user, pass) {
    document.getElementById("entrega").style.display = "flex";
    document.getElementById("userBox").value = user;
    document.getElementById("passBox").value = pass;
}

function fecharEntrega() {
    document.getElementById("entrega").style.display = "none";
}

function copiar(id) {
    let campo = document.getElementById(id);
    campo.select();
    document.execCommand("copy");
    alert("Copiado!");
}
</script>

</body>
</html>
