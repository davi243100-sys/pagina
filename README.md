<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<title>Blox Mundial – Loja de Contas</title>
<style>
    body { font-family: Arial; background:#f1f1f1; padding:20px; }
    h2 { margin-top:30px; }
    .product {
        margin-bottom:18px; padding:12px; border:1px solid #ccc;
        border-radius:10px; background:white;
    }
    .small { opacity:.8; font-size:13px; }
    button {
        width:100%; padding:10px; border:none;
        background:#4CAF50; color:white;
        border-radius:8px; margin-top:10px; cursor:pointer;
    }
    #entrega {
        display:none; position:fixed; top:0; left:0;
        width:100%; height:100%;
        background:rgba(0,0,0,0.6);
        justify-content:center; align-items:center;
    }
    #entregaBox {
        background:white; padding:20px; border-radius:10px;
        width:90%; max-width:350px;
    }
    input {
        width:100%; padding:8px; margin-bottom:10px;
        border:1px solid #aaa; border-radius:6px;
    }
</style>
</head>

<body>

<h2>Contas à Venda</h2>

<!-- CONTA SHARK ANCHOR -->
<div class="product">
    <strong>Shark Anchor + Doug + Gas + Venom</strong>
    <span class="small">Lv. 2800</span>
    <br><span class="small">R$ 40</span>

    <img src="https://i.imgur.com/1QeQZ4t.png"
         style="width:100%; max-width:300px; border-radius:10px; margin-top:12px;">

    <button onclick="abrirEntrega('ClarenceMcintyre4402','valeria2')">
        Comprar
    </button>
</div>

<!-- CONTA BUDDHA FREE -->
<div class="product">
    <strong>Buddha + CDK</strong>
    <span class="small">Lv. 2800</span>
    <br><span class="small" style="color:green;">R$ 0 (FREE)</span>

    <img src="https://i.imgur.com/1QeQZ4t.png"
         style="width:100%; max-width:300px; border-radius:10px; margin-top:12px;">

    <button onclick="abrirEntrega('AlbertGrimes259','secret244')">
        PEGAR GRÁTIS
    </button>
</div>

<!-- JANELA ENTREGA -->
<div id="entrega">
    <div id="entregaBox">
        <h3>Informações da Conta</h3>

        <label>Usuário:</label>
        <input id="usuario" readonly>
        <button onclick="copiar('usuario')">Copiar Usuário</button>

        <label>Senha:</label>
        <input id="senha" readonly>
        <button onclick="copiar('senha')">Copiar Senha</button>

        <button onclick="fecharEntrega()" style="background:#d9534f; margin-top:15px;">Fechar</button>
    </div>
</div>

<script>
function abrirEntrega(user, pass) {
    document.getElementById("usuario").value = user;
    document.getElementById("senha").value = pass;
    document.getElementById("entrega").style.display = "flex";
}

function fecharEntrega() {
    document.getElementById("entrega").style.display = "none";
}

function copiar(id) {
    let input = document.getElementById(id);
    input.select();
    document.execCommand("copy");
}
</script>

</body>
</html>
