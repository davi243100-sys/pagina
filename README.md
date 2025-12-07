<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Loja Blox Mundial</title>
<style>
    body { font-family: Arial; background:#f2f2f2; padding:20px; }
    h2 { margin-top:30px; }
    .section {
        background:white; padding:18px; border-radius:12px;
        border:1px solid #ccc; margin-bottom:25px;
    }
    .product {
        margin-bottom:18px; padding:12px;
        border:1px solid #ddd; border-radius:10px; background:#fff;
    }
    .small { font-size:13px; opacity:.8; }
    button {
        background:#4CAF50; color:white; width:100%; padding:10px;
        border:none; border-radius:8px; cursor:pointer; font-weight:bold;
    }
</style>
</head>
<body>

<section class="section">
<h2>Produtos em destaque</h2>

<!-- FREE Buddha -->
<div class="product">
    <div style="display:flex; justify-content:space-between;">
        <strong>Buddha — Conta FREE</strong>
        <span class="small" style="color:green;">R$ 0</span>
    </div>
    <div class="small">Conta inicial com fruta Buddha.</div>
    <button onclick="abrirEntrega('FREEaccount','free2024')">PEGAR GRÁTIS</button>
</div>

<!-- Shark Anchor + Doug + Venom + Gas + Lv 2800 -->
<div class="product">
    <div style="display:flex; justify-content:space-between;">
        <strong>Shark Anchor + Doug + Gas + Venom + Lv 2800</strong>
        <span class="small">R$ 40</span>
    </div>
    <div class="small">Conta completa e extremamente forte.</div>
    <button onclick="abrirEntrega('ClarenceMcintyre4402','valeria2')">PEGAR CONTA</button>
</div>

<!-- Buddha + CDK + Lv 2800 -->
<div class="product">
    <div style="display:flex; justify-content:space-between;">
        <strong>Buddha + CDK + Level 2800</strong>
        <span class="small">R$ 40</span>
    </div>
    <div class="small">Conta forte pronta para endgame.</div>
    <button onclick="abrirEntrega('AlbertGrimes259','secret244')">PEGAR CONTA</button>
</div>

<!-- Guia Premium -->
<div class="product">
    <div style="display:flex; justify-content:space-between;">
        <strong>Guia Premium</strong><span class="small">R$ 12</span>
    </div>
    <div class="small">E-book com segredos e estratégias.</div>
    <button onclick="abrirEntrega('GuiaPremiumPDF','download2024')">PEGAR GUIA</button>
</div>

<!-- VIP -->
<div class="product">
    <div style="display:flex; justify-content:space-between;">
        <strong>Pacote VIP</strong><span class="small">R$ 60</span>
    </div>
    <div class="small">Bônus exclusivos e prioridade.</div>
    <button onclick="abrirEntrega('VIPAccess','vip2024')">PEGAR VIP</button>
</div>

</section>

<!-- JANELA DE ENTREGA -->
<div id="entrega" style="
    display:none; position:fixed; top:0; left:0; width:100%; height:100%;
    background:rgba(0,0,0,0.6); justify-content:center; align-items:center;">
    <div style="background:white; padding:25px; border-radius:12px; width:320px;">
        <h3>Dados da Conta</h3>

        <p><strong>Usuário:</strong></p>
        <input id="userBox" style="width:100%; padding:8px;" readonly>
        <button onclick="copiar('userBox')">Copiar Usuário</button>

        <p style="margin-top:15px;"><strong>Senha:</strong></p>
        <input id="passBox" style="width:100%; padding:8px;" readonly>
        <button onclick="copiar('passBox')">Copiar Senha</button>

        <button style="background:#d32f2f; margin-top:18px;" onclick="fecharEntrega()">Fechar</button>
    </div>
</div>

<script>
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
