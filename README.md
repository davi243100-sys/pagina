<!doctype html>
<html lang="pt-BR">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Blox Mundial — Loja</title>
  <meta name="description" content="Blox Mundial — Loja digital" />
  <link rel="icon" href="data:;base64,iVBORw0KGgo="> 
  <style>
    :root{--bg:#0f1724;--card:#0b1220;--accent:#06b6d4;--muted:#94a3b8;--glass: rgba(255,255,255,0.03)}
    *{box-sizing:border-box}
    body{margin:0;font-family:Inter, ui-sans-serif, system-ui, -apple-system, 'Segoe UI', Roboto, 'Helvetica Neue', Arial; background:linear-gradient(180deg,#071029 0%, #07162b 100%);color:#e6eef6}
    .container{max-width:1100px;margin:0 auto;padding:28px}
    header{display:flex;align-items:center;justify-content:space-between;padding:14px 0}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#7c3aed);display:flex;align-items:center;justify-content:center;font-weight:700}
    nav a{color:var(--muted);text-decoration:none;margin-left:18px}
    .hero{display:grid;grid-template-columns:1fr 380px;gap:28px;align-items:start;margin-top:22px}
    .card{background:var(--card);border-radius:14px;padding:20px;box-shadow:0 6px 24px rgba(2,6,23,0.7)}
    h1{margin:0 0 6px 0;font-size:28px}
    p.lead{color:var(--muted);margin:0 0 16px}
    .cta{display:flex;gap:12px}
    .btn{background:var(--accent);color:#012;padding:10px 14px;border-radius:10px;font-weight:600;border:none;cursor:pointer}
    .btn.ghost{background:transparent;border:1px solid rgba(255,255,255,0.06);color:var(--muted)}
    .product-list{display:grid;grid-template-columns:repeat(2,1fr);gap:12px;margin-top:12px}
    .product{background:var(--glass);padding:12px;border-radius:10px}
    .small{font-size:13px;color:var(--muted)}
    .side-pay{position:sticky;top:24px}
    label{display:block;font-size:13px;margin-top:8px;color:var(--muted)}
    input,select,textarea{width:100%;padding:10px;margin-top:6px;border-radius:8px;border:none;background:rgba(255,255,255,0.02);color:inherit}
    .section{margin-top:22px}
    .grid3{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    .testimonials{display:grid;grid-template-columns:repeat(3,1fr);gap:12px}
    footer{margin-top:28px;padding:18px 0;color:var(--muted);font-size:14px}
    .promo{background:linear-gradient(90deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:12px;border-radius:10px}
    .partner{display:flex;align-items:center;gap:8px;padding:8px;background:rgba(255,255,255,0.02);border-radius:8px}
    @media(max-width:900px){.hero{grid-template-columns:1fr}.product-list{grid-template-columns:1fr}.testimonials,.grid3{grid-template-columns:1fr}.side-pay{position:static}}
  </style>
</head>
<body>
  <div class="container">
    <header>
      <div class="brand">
        <div class="logo">BM</div>
        <div>
          <div style="font-weight:700">Blox Mundial</div>
          <div class="small">Loja digital — produtos e serviços para Blox Fruits</div>

      <div class="product" style="margin-bottom:18px; padding:12px; border:1px solid #ddd; border-radius:10px; background:#fff;">
        <div style="display:flex; justify-content:space-between; align-items:center;">
          <strong>Pacote VIP</strong>
          <span class="small">R$ 60</span>
        </div>
        <div class="small">Combo de serviços com desconto e prioridade.</div>
      </div>
    </div>
      <nav>
        <a href="#produtos">Produtos</a>
        <a href="#pagamento">Pagamento</a>
        <a href="#provas">Prova social</a>
        <a href="#parceiros">Parceiros</a>
        <a href="#reembolso">Reembolso</a>
      </nav>
    </header>

    <main>
  <div class="section">
    <h3>Produtos em destaque</h3>
    <div class="product-list">

      <div class="product" style="margin-bottom:18px; padding:12px; border:1px solid #ddd; border-radius:10px; background:#fff;">
        <div style="display:flex; justify-content:space-between; align-items:center;">
          <strong>Conta Lv. Alto</strong>
          <span class="small">R$ 40</span>
        </div>
        <div class="small">Conta com progressos e skins. Entrega digital.</div>
      </div>

      <div class="product" style="margin-bottom:18px; padding:12px; border:1px solid #ddd; border-radius:10px; background:#fff;">
        <div style="display:flex; justify-content:space-between; align-items:center;">
          <strong>Guia Premium</strong>
          <span class="small">R$ 12</span>
        </div>
        <div class="small">E-book com dicas e estratégias de Blox Fruits.</div>
      </div>

    </div>
  </div>

      <section class="hero">
        <div>
          <div class="card">
            <h1>Blox Mundial</h1>
            <p class="lead">Bem-vindo à Blox Mundial — loja profissional de produtos digitais. Aqui você encontra serviços e opções para turbinar seu jogo. Trabalhamos com pagamentos via Pix (Nubank) e atendimento rápido pelo Discord.</p>
            <div class="cta">
              <button class="btn" onclick="document.getElementById('pedido').scrollIntoView({behavior:'smooth'})">Fazer pedido</button>
              <a class="btn ghost" href="#reembolso">Política de Reembolso</a>
            </div>

            <div class="section">
              <h3>Produtos em destaque</h3>
              <div class="product-list">
                <div class="product">
                  <div style="display:flex;justify-content:space-between;align-items:center"><strong>Conta Lv. Alto</strong><span class="small">R$ 40</span></div>
                  <div class="small">Conta com progressos e skins. Entrega digital.</div>
                </div>
                <div class="product">
                  <div style="display:flex;justify-content:space-between;align-items:center"><strong>Serviço: Farm</strong><span class="small">R$ 20</span></div>
                  <div class="small">Serviço de farm por horas — entregue como relatório.</div>
                </div>
                <div class="product">
                  <div style="display:flex;justify-content:space-between;align-items:center"><strong>Guia Premium</strong><span class="small">R$ 12</span></div>
                  <div class="small">E-book com dicas e estratégias de Blox Fruits.</div>
                </div>
                <div class="product">
                  <div style="display:flex;justify-content:space-between;align-items:center"><strong>Pacote VIP</strong><span class="small">R$ 60</span></div>
                  <div class="small">Combo de serviços com desconto e prioridade.</div>
                </div>
              </div>
            </div>

            <div class="section">
              <h3>Observação importante</h3>
              <p class="small">A Blox Mundial não incentiva violação dos Termos de Uso de plataformas. Produtos e serviços são entregues de forma digital e podem ter restrições conforme as regras dos jogos e plataformas.</p>
            </div>

          </div>
        </div>

        <aside class="side-pay">
          <div class="card">
            <h3>Pedir agora</h3>
            <form id="pedido" onsubmit="event.preventDefault();simulatePedido()">
              <label>Código da compra
                <input id="codigo" placeholder="Digite o código recebido" required>
              </label>
              <label>Produto
                <select id="produto">
                  <option value="Conta Lv. Alto">Conta Lv. Alto — R$ 40</option>
                  <option value="Serviço: Farm">Serviço: Farm — R$ 20</option>
                  <option value="Guia Premium">Guia Premium — R$ 12</option>
                  <option value="Pacote VIP">Pacote VIP — R$ 60</option>
                </select>
              </label>
              <label>Nome / ID do jogo<input id="nomeid" placeholder="Ex: Pedro123" required></label>
              <label>Comprovante (opcional)</label>
              <textarea id="obs" rows="3" placeholder="Observações, prints, etc."></textarea>
              <label>Forma de pagamento<select id="pagamentoMethod"><option>Pix (Nubank)</option><option>Mercado Pago</option><option>PayPal</option></select></label>
              <div style="margin-top:10px;display:flex;gap:8px">
                <button class="btn" type="submit">Enviar pedido</button>
                <button class="btn ghost" type="button" onclick="window.location='#provas'">Ver provas</button>
              </div>
            </form>
            <div id="pedido-msg" style="margin-top:12px;font-size:13px;color:var(--muted)"></div>
          </div>

          
            <div class="small" style="margin-top:8px">Ao pagar: envie o comprovante no Discord/WhatsApp com seu nome/ID.</div>
            <div style="margin-top:8px"><a class="btn" href="#">Copiar Pix</a></div>
          </div>

        </aside>

          <div class="conta-info" style="margin-top:20px; padding:14px; border-radius:10px; background:#fff; border:1px solid #ddd;">
      <h3>Conta à Venda</h3>
      <p><strong>Conta:</strong> Buddha</p>
      <p><strong>Espada:</strong> CDK</p>
      <p><strong>Nível:</strong> 2800</p>
      <img src="https://i.imgur.com/1QeQZ4t.png" alt="Blox Fruits" style="width:100%; max-width:300px; margin-top:12px; border-radius:10px;" />
    </div>
  </section>

      <section id="provas" class="section">
        <h2>Prova social</h2>
        <div class="testimonials">
          <div class="card">
            <strong>"Atendimento super rápido"</strong>
            <div class="small" style="margin-top:8px">Pedro A. — entrega confirmada</div>
          </div>
          <div class="card">
            <strong>"Melhor loja, recomendo"</strong>
            <div class="small" style="margin-top:8px">Luan G. — 5 estrelas</div>
          </div>
          <div class="card">
            <strong>Vídeos e prints</strong>
            <div class="small" style="margin-top:8px">Mostre aqui seus vídeos curtos (TikTok/Shorts) e prints com dados sensíveis censurados.</div>
          </div>
        </div>
      </section>

      <section id="promocoes" class="section">
        <h2>Promoções</h2>
        <div class="grid3">
          <div class="promo card">
            <strong>Combo Semana Gamer</strong>
            <div class="small">10% OFF acima de R$30</div>
          </div>
          <div class="promo card">
            <strong>Indique um amigo</strong>
            <div class="small">Ganhe 5% de desconto por indicação</div>
          </div>
          <div class="promo card">
            <strong>Cliente VIP</strong>
            <div class="small">Após 3 compras, cupom de 15% OFF</div>
          </div>
        </div>
      </section>

      <section id="parceiros" class="section">
        <h2>Parceiros / Influenciadores</h2>
        <div style="display:flex;gap:12px;flex-wrap:wrap">
          <div class="partner">
            <div style="width:40px;height:40px;background:rgba(255,255,255,0.02);border-radius:8px;display:flex;align-items:center;justify-content:center">Ti</div>
            <div>
              <div style="font-weight:700">@tiktok_influencer</div>
              <div class="small">Cupom: TIKTOK10 — comissão por venda</div>
            </div>
          </div>

          <div class="partner">
            <div style="width:40px;height:40px;background:rgba(255,255,255,0.02);border-radius:8px;display:flex;align-items:center;justify-content:center">Yt</div>
            <div>
              <div style="font-weight:700">Streamers locais</div>
              <div class="small">Parcerias para sorteios e lives</div>
            </div>
          </div>

        </div>
      </section>

      <section id="reembolso" class="section">
        <h2>Política de Reembolso</h2>
        <div class="card">
          <p class="small">A Blox Mundial trabalha com produtos e serviços digitais. Veja nossas regras:</p>
          <ul class="small">
            <li><strong>Reembolso possível</strong> se o produto não foi entregue ou houver divergência entre o que foi anunciado e o entregue.</li>
            <li><strong>Reembolso não garantido</strong> quando o produto já foi entregue ou houver evidências de uso indevido.</li>
            <li>Solicitações devem ser feitas com comprovante de pagamento, nome/ID e motivo do pedido.</li>
            <li>Resposta em até 24 horas (suporte online).</li>
          </ul>
        </div>
      </section>

      <section class="pix-section" style="margin-top:20px; padding:16px; border:1px solid #ccc; border-radius:12px; background:#fafafa;">
    <h2>Pagamento via Pix</h2>
    <p><strong>Copie e cole o código Pix:</strong></p>
    <textarea style="width:100%; height:120px; padding:10px; border-radius:8px;">00020126360014BR.GOV.BCB.PIX0114+5555999231517520400005303986540521.005802BR5925David Luiz Turani Bechene6009SAO PAULO62140510nWJgB4hhTi63042A0A</textarea>

    <div class="conta-info" style="margin-top:20px; padding:14px; border-radius:10px; background:#fff; border:1px solid #ddd;">
      <h3>Conta à Venda</h3>
      <p><strong>Conta:</strong> Shark Anchor</p>
      <p><strong>Nível:</strong> 2800</p>
      <p><strong>Frutas:</strong> Doug (maestria 1), Gas, Venom</p>
      <img src="https://i.imgur.com/1QeQZ4t.png" alt="Blox Fruits" style="width:100%; max-width:300px; margin-top:12px; border-radius:10px;" />
    </div>
  </section>
  
  <section class="section" id="promocoes">
    <h2>Promoções</h2>
    <div class="grid3">
      <div class="promo card" style="padding:12px; border:1px solid #ddd; border-radius:10px; background:#fff;">
        <strong>Combo Semana Gamer</strong>
        <div class="small">10% OFF acima de R$30</div>
      </div>
      <div class="promo card" style="padding:12px; border:1px solid #ddd; border-radius:10px; background:#fff;">
        <strong>Indique um amigo</strong>
        <div class="small">Ganhe 5% de desconto por indicação</div>
      </div>
    </div>
  </section>

  <script>
    // Adiciona imagens aos produtos
    document.querySelectorAll('.product').forEach((p)=>{
      if(!p.querySelector('img')){
        const img=document.createElement('img');
        img.src="https://i.imgur.com/1QeQZ4t.png";
        img.style="width:100%;max-width:250px;margin-top:10px;border-radius:10px;";
        p.appendChild(img);
      }
    });
  </script>

</main>

    <footer>
      <div style="display:flex;justify-content:space-between;align-items:center;gap:12px;flex-wrap:wrap">
        <div>
          <div style="font-weight:700">Blox Mundial</div>
          <div class="small">Contato: Discord / WhatsApp</div>
        </div>
        <div class="small">© Blox Mundial — Todos os direitos reservados</div>
      </div>
    </footer>
  </div>

  <script>
    function simulatePedido(){
      const produto = document.getElementById('produto').value;
      const nomeid = document.getElementById('nomeid').value;
      const msg = document.getElementById('pedido-msg');
      if(!nomeid){msg.textContent='Informe seu Nome/ID para prosseguir.';return}
      msg.textContent = 'Pedido recebido: '+produto+" — Aguarde instruções de pagamento no Discord/WhatsApp.";
      // Início da contagem de tempo para pagamento
      startTimer()
      setTimeout(()=>{
        msg.textContent += ' (Simulação: lembre-se de confirmar o Pix antes de liberar qualquer produto.)';
      },900)
    }

    // Função simples para copiar Pix
    document.querySelectorAll('.btn').forEach(b=>{
      if(b.textContent.trim()==='Copiar Pix'){
        b.addEventListener('click',()=>{
          const pix = document.getElementById('pix-key').textContent;
          navigator.clipboard?.writeText(pix).then(()=>alert('Pix copiado: '+pix)).catch(()=>alert('Não foi possível copiar automaticamente.'))
        })
      }
    })
  
    let countdown;
    function startTimer(){
      clearInterval(countdown);
      let time = 600; // 10 minutos
      const msg = document.getElementById('pedido-msg');
      countdown = setInterval(()=>{
        const min = Math.floor(time/60);
        const sec = time%60;
        msg.textContent = `Pagamento pendente. Tempo restante: ${min}m ${sec}s`;
        time--;
        if(time < 0){
          clearInterval(countdown);
          msg.textContent = 'Tempo expirado. Faça o pedido novamente.';
        }
      },1000);
    }
</script>
</body>
  <!-- Modal de Entrega de Conta -->
  <div id="entregaModal" style="display:none; position:fixed; top:0; left:0; width:100%; height:100%; background:rgba(0,0,0,0.6); backdrop-filter:blur(4px); justify-content:center; align-items:center;">
    <div style="background:#fff; padding:20px; border-radius:12px; width:90%; max-width:400px; text-align:center;">
      <h2>Detalhes da Conta</h2>

      <h3>Conta Buddha</h3>
      <p><strong>Usuário:</strong> ClarenceMcintyre4402</p>
      <textarea style="width:100%; padding:8px; border-radius:8px;">ClarenceMcintyre4402</textarea>
      <p><strong>Senha:</strong> valeria2</p>
      <textarea style="width:100%; padding:8px; border-radius:8px;">valeria2</textarea>

      <hr style="margin:18px 0;">

      <h3>Conta Shark Anchor</h3>
      <p><strong>Usuário:</strong> AlbertGrimes259</p>
      <textarea style="width:100%; padding:8px; border-radius:8px;">AlbertGrimes259</textarea>
      <p><strong>Senha:</strong> secret244</p>
      <textarea style="width:100%; padding:8px; border-radius:8px;">secret244</textarea>

      <button onclick="document.getElementById('entregaModal').style.display='none'" style="margin-top:16px; padding:10px 20px; border:none; border-radius:8px; background:#333; color:#fff; cursor:pointer;">Fechar</button>
    </div>
  </div>
</html>
