<!DOCTYPE html>
<html lang="pt-br">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Delícias da Jô - PDV Master</title>
    <style>
        :root { 
            --primary: #2c3e50; --success: #27ae60; --danger: #e74c3c; 
            --bg: #f4f7f6; --white: #ffffff; --accent: #3498db; --wpp: #25d366; --file: #9b59b6;
        }
        body { font-family: 'Segoe UI', sans-serif; background: var(--bg); margin: 0; }
        #loginOverlay { position: fixed; inset: 0; background: var(--primary); z-index: 9999; display: flex; align-items: center; justify-content: center; }
        .login-box { background: var(--white); padding: 30px; border-radius: 20px; width: 90%; max-width: 320px; text-align: center; }
        header { background: var(--white); padding: 10px; box-shadow: 0 2px 10px rgba(0,0,0,0.1); position: sticky; top: 0; z-index: 100; }
        .nav-tabs { display: flex; justify-content: center; gap: 5px; margin-top: 10px; flex-wrap: wrap; }
        .tab-btn { background: #eee; padding: 10px; border-radius: 8px; border: none; font-weight: bold; cursor: pointer; flex: 1; min-width: 100px; }
        .tab-btn.active { background: var(--accent); color: white; }
        .container { padding: 15px; max-width: 1200px; margin: 0 auto; }
        .tab-content { display: none; }
        .tab-content.active { display: block; }
        .box { background: var(--white); padding: 20px; border-radius: 15px; box-shadow: 0 4px 15px rgba(0,0,0,0.05); margin-bottom: 20px; }
        .grid { display: grid; grid-template-columns: repeat(auto-fill, minmax(155px, 1fr)); gap: 12px; }
        .card { background: var(--white); border: 1px solid #eee; padding: 12px; border-radius: 15px; text-align: center; position: relative; }
        button { cursor: pointer; border-radius: 8px; font-weight: bold; border: none; transition: 0.2s; }
        .btn-venda { background: var(--success); color: white; width: 100%; padding: 12px; margin-top: 8px; }
        .btn-wpp { background: var(--wpp); color: white; width: 100%; padding: 15px; margin-top: 8px; display: flex; align-items: center; justify-content: center; gap: 8px; }
        .btn-file { background: var(--file); color: white; width: 100%; padding: 15px; margin-top: 8px; display: flex; align-items: center; justify-content: center; gap: 8px; }
        input, select { width: 100%; padding: 12px; margin: 8px 0; border: 1px solid #ddd; border-radius: 8px; box-sizing: border-box; }
        .ticket { background: #fffdf0; border: 1px solid #e6dbac; padding: 10px; margin-bottom: 8px; border-radius: 8px; font-family: monospace; font-size: 12px; }
        .caixa-final { background: var(--primary); color: white; padding: 20px; border-radius: 15px; text-align: center; margin-bottom: 10px; line-height: 1.6; }
        .admin-only { display: none; }
        #displayTroco { font-size: 1.2rem; margin-top: 10px; font-weight: bold; text-align: center; }
    </style>
</head>
<body>

<div id="loginOverlay">
    <div class="login-box">
        <h2>🥖 Delícias da Jô</h2>
        <input id="userName" placeholder="Seu Nome">
        <select id="userPerfil" onchange="document.getElementById('passArea').style.display = (this.value=='adm'?'block':'none')">
            <option value="operador">Operador</option>
            <option value="adm">Administrador (Jô)</option>
        </select>
        <div id="passArea" style="display:none"><input id="userPass" type="password" placeholder="Senha ADM"></div>
        <button class="btn-venda" style="background:var(--accent)" onclick="logar()">ENTRAR NO SISTEMA</button>
    </div>
</div>

<header id="mainHeader" style="display:none">
    <div style="display:flex; justify-content: space-between; align-items:center; max-width:1200px; margin:0 auto">
        <b>🍞 JÔ SISTEMA</b>
        <span id="displayUser" style="font-size:12px; font-weight:bold"></span>
    </div>
    <div class="nav-tabs">
        <button class="tab-btn active" onclick="openTab(event, 'tabVendas')">VENDAS</button>
        <button class="tab-btn admin-only" onclick="openTab(event, 'tabCad')">CADASTRAR</button>
        <button class="tab-btn" onclick="openTab(event, 'tabRel')">RELATÓRIO</button>
    </div>
</header>

<div class="container" id="mainContent" style="display:none">
    <div id="tabVendas" class="tab-content active">
        <div id="vitrine" class="grid"></div>
        <div class="box" style="margin-top:20px">
            <h3>🛒 Pedido</h3>
            <div id="carrinhoItens"></div>
            <h2 id="totalVenda" style="text-align: center;">R$ 0.00</h2>
            <hr>
            <input id="inputPago" type="number" placeholder="Valor que o cliente deu" oninput="calcularTroco()">
            <div id="displayTroco"></div>
            <button class="btn-venda" onclick="finalizarVenda()">CONCLUIR E LIMPAR</button>
        </div>
    </div>

    <div id="tabCad" class="tab-content">
        <div class="box">
            <h3>📦 Novo Produto</h3>
            <input id="cadNome" placeholder="Nome do Produto">
            <input id="cadPreco" type="number" step="0.01" placeholder="Preço Unitário">
            <input id="cadEstoque" type="number" placeholder="Estoque Inicial">
            <button class="btn-venda" style="background:var(--accent)" onclick="cadastrarProduto()">SALVAR NO BANCO</button>
        </div>
    </div>

    <div id="tabRel" class="tab-content">
        <div class="box">
            <div id="resumoFinanceiro" class="caixa-final"></div>
            <button class="btn-wpp" onclick="enviarWhatsApp()">📱 ENVIAR WHATSAPP</button>
            <button class="btn-file" onclick="gerarArquivoRelatorio()">📄 GERAR ARQUIVO TXT</button>
            <div class="admin-only">
                <button onclick="limparDados()" style="width:100%; color:red; background:none; border:1px solid red; margin-top:15px; padding:10px;">ZERAR SISTEMA</button>
            </div>
        </div>
        <div class="box">
            <h3>📜 Histórico de Hoje</h3>
            <div id="listaLogs"></div>
        </div>
    </div>
</div>

<script>
    let logado = ""; let nivel = "operador";
    let produtos = JSON.parse(localStorage.getItem("j_prod")) || [];
    let historico = JSON.parse(localStorage.getItem("j_hist")) || [];
    let carrinho = [];

    function logar() {
        const nome = document.getElementById("userName").value;
        const pfe = document.getElementById("userPerfil").value;
        const pass = document.getElementById("userPass").value;
        if(!nome) return alert("Digite seu nome");
        if(pfe === 'adm' && pass !== 'jo123') return alert("Senha Incorreta");
        logado = nome; nivel = pfe;
        if(nivel === 'adm') document.querySelectorAll('.admin-only').forEach(e => e.style.display = 'block');
        document.getElementById("loginOverlay").style.display = 'none';
        document.getElementById("mainHeader").style.display = 'block';
        document.getElementById("mainContent").style.display = 'block';
        document.getElementById("displayUser").innerText = logado;
        render(); renderLogs();
    }

    function openTab(evt, tabName) {
        document.querySelectorAll(".tab-content").forEach(t => t.classList.remove("active"));
        document.querySelectorAll(".tab-btn").forEach(b => b.classList.remove("active"));
        document.getElementById(tabName).classList.add("active");
        evt.currentTarget.classList.add("active");
    }

    function cadastrarProduto() {
        const n = document.getElementById("cadNome").value;
        const p = parseFloat(document.getElementById("cadPreco").value);
        const e = parseInt(document.getElementById("cadEstoque").value) || 0;
        if(!n || isNaN(p)) return;
        produtos.push({ id: Date.now(), nome: n, preco: p, estoque: e });
        salvar(); render();
        document.getElementById("cadNome").value = ""; document.getElementById("cadPreco").value = "";
    }

    function addCarrinho(id) {
        const p = produtos.find(x => x.id === id);
        let q = prompt(`Quantos "${p.nome}"?`, "1");
        if (!q) return;
        let qtd = parseInt(q);
        if (qtd > p.estoque) return alert(`Só temos ${p.estoque} no estoque!`);
        carrinho.push({ id: p.id, nome: p.nome, preco: p.preco, qtd: qtd, subtotal: p.preco * qtd });
        p.estoque -= qtd;
        render(); atualizarCarrinhoUI();
    }

    function calcularTroco() {
        const total = parseFloat(document.getElementById("totalVenda").innerText.replace("R$ ",""));
        const pago = parseFloat(document.getElementById("inputPago").value) || 0;
        const display = document.getElementById("displayTroco");
        if(pago > 0) {
            const troco = pago - total;
            display.innerText = troco >= 0 ? `Troco: R$ ${troco.toFixed(2)}` : `Falta: R$ ${Math.abs(troco).toFixed(2)}`;
            display.style.color = troco >= 0 ? "green" : "red";
        } else { display.innerText = ""; }
    }

    function entradaEstoque(id) {
        const p = produtos.find(x => x.id === id);
        let q = prompt(`Adicionar quanto ao estoque de ${p.nome}?`);
        if(!q) return;
        p.estoque += parseInt(q);
        salvar(); render();
    }

    function registrarPerda(id) {
        const p = produtos.find(x => x.id === id);
        let q = prompt(`Quantidade que estragou de ${p.nome}:`);
        if(!q) return;
        let qtd = parseInt(q);
        if(qtd > p.estoque) return alert("Não pode perder mais do que tem!");
        let vPerda = p.preco * qtd;
        p.estoque -= qtd;
        historico.push({ t: 'PERDA', desc: `${qtd}x ${p.nome}`, v: vPerda, h: new Date().toLocaleTimeString(), op: logado });
        salvar(); render(); renderLogs();
    }

    function atualizarCarrinhoUI() {
        const d = document.getElementById("carrinhoItens");
        d.innerHTML = ""; let t = 0;
        carrinho.forEach(i => {
            t += i.subtotal;
            d.innerHTML += `<div class="ticket"><b>${i.qtd}x</b> ${i.nome} - R$ ${i.subtotal.toFixed(2)}</div>`;
        });
        document.getElementById("totalVenda").innerText = `R$ ${t.toFixed(2)}`;
        calcularTroco();
    }

    function finalizarVenda() {
        if(carrinho.length === 0) return;
        const t = carrinho.reduce((a,b) => a + b.subtotal, 0);
        const res = carrinho.map(i => `${i.qtd}x ${i.nome}`).join(", ");
        historico.push({ t: 'VENDA', desc: res, v: t, h: new Date().toLocaleTimeString(), op: logado });
        carrinho = []; document.getElementById("inputPago").value = ""; 
        salvar(); atualizarCarrinhoUI(); renderLogs();
    }

    function render() {
        const v = document.getElementById("vitrine");
        v.innerHTML = "";
        produtos.forEach(p => {
            v.innerHTML += `<div class="card">
                <b>${p.nome}</b><br>R$ ${p.preco.toFixed(2)}<br>
                <small>Est: ${p.estoque}</small>
                <button class="btn-venda" onclick="addCarrinho(${p.id})">🛒 VENDER</button>
                <div class="admin-only" style="display:${nivel=='adm'?'flex':'none'}; gap:4px; margin-top:5px">
                    <button onclick="entradaEstoque(${p.id})" style="flex:1; background:#eee; font-size:10px; padding:5px;">+ EST</button>
                    <button onclick="registrarPerda(${p.id})" style="flex:1; background:#ffebeb; color:red; font-size:10px; padding:5px;">PERDA</button>
                </div>
            </div>`;
        });
    }

    function renderLogs() {
        const l = document.getElementById("listaLogs");
        l.innerHTML = ""; let vT = 0; let pT = 0;
        historico.slice().reverse().forEach(h => {
            if(h.t === 'VENDA') vT += h.v; else pT += h.v;
            l.innerHTML += `<div class="ticket" style="border-left:4px solid ${h.t=='VENDA'?'green':'red'}">
                <b>${h.h}</b> | ${h.t} | <b>R$ ${h.v.toFixed(2)}</b><br>${h.desc}
            </div>`;
        });
        document.getElementById("resumoFinanceiro").innerHTML = `
            VENDAS: R$ ${vT.toFixed(2)}<br>
            PERDAS: R$ ${pT.toFixed(2)}<br>
            <b style="font-size:1.4rem">LÍQUIDO: R$ ${(vT - pT).toFixed(2)}</b>
        `;
    }

    function gerarTextoRelatorio() {
        let vT = 0; let pT = 0; 
        let listaVendas = ""; let listaPerdas = "";
        
        historico.forEach(h => {
            if(h.t === 'VENDA') {
                vT += h.v;
                listaVendas += `✅ [${h.h}] R$ ${h.v.toFixed(2)} (${h.desc})\n`;
            } else {
                pT += h.v;
                listaPerdas += `❌ [${h.h}] R$ ${h.v.toFixed(2)} (${h.desc})\n`;
            }
        });

        return `🥖 *FECHAMENTO DELÍCIAS DA JÔ* 🥖\n` +
               `📅 Data: ${new Date().toLocaleDateString()}\n` +
               `👤 Op: ${logado}\n\n` +
               `💰 *VENDAS DO DIA:*\n${listaVendas || "Nenhuma venda\n"}\n` +
               `📉 *PERDAS REGISTRADAS:*\n${listaPerdas || "Nenhuma perda\n"}\n` +
               `---------------------------\n` +
               `💵 TOTAL VENDAS: R$ ${vT.toFixed(2)}\n` +
               `💸 TOTAL PERDAS: R$ ${pT.toFixed(2)}\n` +
               `✅ *SALDO LÍQUIDO: R$ ${(vT - pT).toFixed(2)}*`;
    }

    function gerarArquivoRelatorio() {
        const blob = new Blob([gerarTextoRelatorio()], { type: 'text/plain' });
        const a = document.createElement('a');
        a.href = window.URL.createObjectURL(blob);
        a.download = `Relatorio-Jo.txt`;
        a.click();
    }

    function enviarWhatsApp() {
        const texto = encodeURIComponent(gerarTextoRelatorio());
        window.open(`https://api.whatsapp.com/send?phone=554699854014&text=${texto}`, '_blank');
    }

    function salvar() { localStorage.setItem("j_prod", JSON.stringify(produtos)); localStorage.setItem("j_hist", JSON.stringify(historico)); }
    function limparDados() { if(confirm("Deseja mesmo limpar tudo?")) { historico = []; salvar(); renderLogs(); } }
</script>
</body>
</html>
