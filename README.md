<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8" />
<meta name="viewport" content="width=device-width, initial-scale=1" />
<title>Blox Mundial - Loja</title>

<style>
 body { font-family: Arial, sans-serif; background:#f2f2f2; margin:0; padding:0; }
 header { background:#111; color:#fff; padding:18px; text-align:center; font-size:22px; }
 main { padding:20px; }
 .card { background:#fff; padding:15px; border-radius:10px; margin-bottom:15px; border:1px solid #ccc; }
 button { padding:10px 15px; border:none; border-radius:8px; background:#111; color:#fff; cursor:pointer; }
 .input { width:100%; padding:10px; border-radius:8px; border:1px solid #ccc; margin-top:6px; }

 /* Modal */
 #modalPagamento, #modalEntrega {
   display:none; position:fixed; top:0; left:0; width:100%; height:100%; 
   background:rgba(0,0,0,0.6); backdrop-filter:blur(3px);
   justify-content:center; align-items:center;
 }
 .modal-content {
   background:#fff; padding:20px; border-radius:12px; width:90%; max-width:400px; text-align:center;
 }
 textarea { width:100%; padding:8px; border-radius:8px; }

 #timer { font-weight:bold; color:red; margin-top:10px; font-size:18px; }
 img{border-radius:10px;margin-top:10px;width:100%;max-width:250px;}
</style>
</head>
<body>
<header>Blox Mundial - Loja de Contas</header>

<main>

<h2>Selecione o produto</h2>
<div class="card">
 <select id="produto" class="input">
   <option value="conta1">Shark Anchor + Lv 2800 + Doug + Gas + Venom</option>
   <option value="conta2">Buddha + CDK + Lv 2800</option>
 </select>
 <button onclick="abrirPagamento()">Comprar</button>
</div>

<!-- MODAL PAGAMENTO -->
<div id="modalPagamento">
 <div class="modal-content">
   <h3>Pagamento via PIX</h3>
   <p>Use o QR Code ou copie o código Pix abaixo:</p>

   <img src="https://i.imgur.com/0X2aFj7.png" alt="QR PIX" />

   <textarea id="codigoPIX">00020126360014BR.GOV.BCB.PIX0114+5555999231517520400005303986540521.005802BR5925David Luiz Turani Bechene6009SAO PAULO62140510nWJgB4hhTi63042A0A</textarea>

   <button onclick="copiarPix()">Copiar código Pix</button>

   <div id="timer"></div>

   <button style="margin-top:12px" onclick="abrirEntrega()">Já paguei</button>
   <button style="background:#444;margin-top:10px" onclick="fecharPagamento()">Fechar</button>
 </div>
</div>

<!-- MODAL ENTREGA DE CONTAS -->
<div id="modalEntrega">
 <div class="modal-content">
   <h3>Dados da Conta Liberada</h3>

   <!-- CONTA 1 -->
   <div id="conta1Dados" style="display:none;">
     <h4>Shark Anchor</h4>
     <p><strong>Usuário:</strong></p>
     <textarea>AlbertGrimes259</textarea>
     <p><strong>Senha:</strong></p>
     <textarea>secret244</textarea>
   </div>

   <!-- CONTA 2 -->
   <div id="conta2Dados" style="display:none;">
     <h4>Buddha + CDK</h4>
     <p><strong>Usuário:</strong></p>
     <textarea>ClarenceMcintyre4402</textarea>
     <p><strong>Senha:</strong></p>
     <textarea>valeria2</textarea>
   </div>

   <button style="margin-top:12px" onclick="fecharEntrega()">Fechar</button>
 </div>
</div>

</main>

<script>
function abrirPagamento(){
 document.getElementById("modalPagamento").style.display="flex";
 iniciarTimer();
}
function fecharPagamento(){ document.getElementById("modalPagamento").style.display="none"; }

function copiarPix(){
 let copy = document.getElementById("codigoPIX");
 copy.select();
 document.execCommand("copy");
 alert("Código Pix copiado!");
}

// TIMER 5 MINUTOS
let tempo = 300;
function iniciarTimer(){
 tempo = 300;
 let display = document.getElementById("timer");
 let countdown = setInterval(function(){
   let min = Math.floor(tempo/60);
   let sec = tempo % 60;
   if(sec < 10) sec = "0"+sec;
   display.innerHTML = `Tempo para pagamento: ${min}:${sec}`;
   tempo--;
   if(tempo < 0){ clearInterval(countdown); display.innerHTML = "Tempo expirado"; }
 },1000);
}

function abrirEntrega(){
 document.getElementById("modalPagamento").style.display="none";
 document.getElementById("modalEntrega").style.display="flex";

 let produto = document.getElementById("produto").value;
 document.getElementById("conta1Dados").style.display = (produto=="conta1")?"block":"none";
 document.getElementById("conta2Dados").style.display = (produto=="conta2")?"block":"none";
}
function fecharEntrega(){ document.getElementById("modalEntrega").style.display="none"; }
</script>

</body>
</html>
