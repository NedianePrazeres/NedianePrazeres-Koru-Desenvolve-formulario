# NedianePrazeres-Koru-Desenvolve-formulario
meu primeiro formulário inclusivo: pessoas com necessidades especiais e pessoas glbtqia+
<img width="681" height="858" alt="image" src="https://github.com/user-attachments/assets/8a42124b-b0eb-477f-8989-fb69b381669d" />
<!DOCTYPE html>
<html lang="pt-BR">

<head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Formulário de Acesso</title>
    <style>
        body {
            font-family: Arial, sans-serif;
            margin: 0;
            padding: 20px;
            background-color: #f9f9f9;
            transition: background 0.5s ease;
        }

        .boas-vindas {
            text-align: center;
            margin-bottom: 30px;
        }

        form {
            max-width: 500px;
            margin: auto;
            background-color: #fff;
            padding: 20px;
            border-radius: 8px;
            box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
        }

        h1 {
            text-align: center;
            margin-bottom: 20px;
        }

        label {
            display: block;
            margin-top: 15px;
            font-weight: bold;
        }

        input {
            width: 100%;
            padding: 10px;
            margin-top: 5px;
            border: 1px solid #ccc;
            border-radius: 4px;
        }

        button[type="submit"],
        .dark-toggle {
            width: 100%;
            padding: 10px;
            margin-top: 20px;
            background-color: #0078D4;
            color: white;
            border: none;
            border-radius: 4px;
            font-size: 16px;
            cursor: pointer;
        }

        button:hover {
            background-color: #005ea2;
        }

        a {
            display: block;
            margin-top: 10px;
            text-align: center;
            color: #0078D4;
            text-decoration: none;
        }

        a:hover {
            text-decoration: underline;
        }

        .identity-buttons {
            display: flex;
            flex-wrap: wrap;
            gap: 10px;
            margin-top: 30px;
        }

        .identity-buttons button {
            flex: 1 1 45%;
            padding: 10px;
            border: none;
            border-radius: 6px;
            color: white;
            font-weight: bold;
            cursor: pointer;
        }

        .identity-buttons button:focus {
            outline: 3px solid #333;
        }

        .rainbow {
            background: linear-gradient(to right, red, orange, yellow, green, blue, indigo, violet);
        }

        .trans {
            background: linear-gradient(to right, #5BCEFA, #F5A9B8, white, #F5A9B8, #5BCEFA);
        }

        .nonbinary {
            background: linear-gradient(to right, #FFF430, #FFFFFF, #9C59D1, #000000);
        }

        .lesbian {
            background: linear-gradient(to right, #D52D00, #FF9A56, #FFFFFF, #D362A4, #A30262);
        }

        .bisexual {
            background: linear-gradient(to right, #D60270, #D60270, #9B4F96, #0038A8, #0038A8);
        }

        .pansexual {
            background: linear-gradient(to right, #FF218C, #FFD800, #21B1FF);
        }

        .asexual {
            background: linear-gradient(to right, #000000, #A3A3A3, #FFFFFF, #800080);
        }

        body.dark-mode {
            background-color: #121212;
            color: #f0f0f0;
        }

        form.dark-mode {
            background-color: #1e1e1e;
            color: #f0f0f0;
        }

        #mensagem {
            margin-top: 20px;
            text-align: center;
            font-size: 18px;
            font-weight: bold;
        }
    </style>
</head>

<body>
    <section class="boas-vindas" aria-label="Mensagem de boas-vindas">
        <h2>Bem-vinde ao nosso espaço inclusivo 🌈</h2>
        <p>Este formulário foi criado com carinho para acolher todas as identidades. Sinta-se livre, respeitado e
            representado.</p>
    </section>

    <form aria-labelledby="form-title" onsubmit="enviarLogin(event)">
        <h1 id="form-title">Acesso à sua conta</h1>

        <label for="usuario">Nome de usuário</label>
        <input type="text" id="usuario" name="usuario" autocomplete="username" required />

        <label for="senha">Senha</label>
        <input type="password" id="senha" name="senha" autocomplete="current-password" required />

        <button type="submit" aria-label="Enviar login">Continuar</button>

        <a href="#" aria-label="Recuperar senha">Esqueci a senha</a>
        <a href="#" aria-label="Criar nova conta">Ainda não sou cliente</a>

        <div class="identity-buttons" aria-label="Seleção de identidade LGBTQIA+">
            <p>Identifique-se com sua bandeira:</p>
            <button type="button" class="rainbow"
                onclick="mostrarMensagem('LGBTQIA+', 'linear-gradient(to right, red, orange, yellow, green, blue, indigo, violet)')">LGBTQIA+</button>
            <button type="button" class="trans"
                onclick="mostrarMensagem('Trans', 'linear-gradient(to right, #5BCEFA, #F5A9B8, #A30262, #F5A9B8, #5BCEFA)')">Trans</button>
            <button type="button" class="nonbinary"
                onclick="mostrarMensagem('Não-binárie', 'linear-gradient(to right, #FFF430, #000000, #9C59D1, #000000)')">Não-binárie</button>
            <button type="button" class="lesbian"
                onclick="mostrarMensagem('Lésbica', 'linear-gradient(to right, #D52D00, #FF9A56, #000000, #D362A4, #A30262)')">Lésbica</button>
            <button type="button" class="bisexual"
                onclick="mostrarMensagem('Bissexual', 'linear-gradient(to right, #D60270, #D60270, #9B4F96, #0038A8, #0038A8)')">Bissexual</button>
            <button type="button" class="pansexual"
                onclick="mostrarMensagem('Pansexual', 'linear-gradient(to right, #FF218C, #FFD800, #21B1FF)')">Pansexual</button>
            <button type="button" class="asexual"
                onclick="mostrarMensagem('Assexual', 'linear-gradient(to right, #000000, #A3A3A3, #FFFFFF, #800080)')">Assexual</button>
        </div>

        <button type="button" class="dark-toggle" onclick="alternarModo()">Alternar modo escuro</button>

        <div id="mensagem" role="status" aria-live="polite"></div>
    </form>

    <!-- VLibras: Tradução em Libras -->
    <div vw class="enabled">
        <div vw-access-button class="active"></div>
        <div vw-plugin-wrapper>
            <div class="vw-plugin-top-wrapper"></div>
        </div>
    </div>
    <script src="https://vlibras.gov.br/app/vlibras-plugin.js"></script>
    <script>
        new window.VLibras.Widget('https://vlibras.gov.br/app');
    </script>

    <script>
        function mostrarMensagem(identidade, corFundo) {
            const mensagem = document.getElementById("mensagem");
            mensagem.textContent = `Bem-vinde, pessoa ${identidade}! 🌈 Você é muito bem acolhida aqui.`;
            document.body.style.background = corFundo;
            localStorage.setItem("identidadeSelecionada", identidade);
            localStorage.setItem("corFundoSelecionada", corFundo);
        }

        function alternarModo() {
            document.body.classList.toggle("dark-mode");
            document.querySelector("form").classList.toggle("dark-mode");
        }

        function enviarLogin(event) {
            event.preventDefault();
            document.getElementById("mensagem").textContent = "Login enviado com sucesso!";
        }

        window.onload = function () {
            const identidade = localStorage.getItem("identidadeSelecionada");
            const cor = localStorage.getItem("corFundoSelecionada");
            if (identidade && cor) {
                mostrarMensagem(identidade, cor);
            }
        };

    </script>
    <!-- Seção opcional: necessidades/condições especiais -->
    <section class="acessibilidade" style="text-align:center; margin-top:40px;">
        <p><strong>Você possui alguma necessidade/condição especial? Qual?</strong></p>
        <button type="button" onclick="mostrarAcessibilidade(true)">Sim</button>
        <button type="button" onclick="mostrarAcessibilidade(false)">Não</button>
        <div id="opcoesAcessibilidade" style="display:none; margin-top:15px;">
            <label>
                <input type="checkbox" onchange="ativarLibras(this)" aria-label="Ativar tradução em Libras">
                Surdez (Libras)
            </label><br>
            <label>
                <input type="checkbox" onchange="ativarContraste(this)" aria-label="Ativar modo alto contraste">
                Deficiência visual (Alto contraste)
            </label><br>
            <label>
                <input type="checkbox" onchange="ativarLeitor(this)" aria-label="Ativar leitor de tela">
                Deficiência motora (Leitor de tela)
            </label>
        </div>
    </section>

    <script>
        function mostrarAcessibilidade(temNecessidade) {
            const opcoes = document.getElementById("opcoesAcessibilidade");
            opcoes.style.display = temNecessidade ? "block" : "none";
        }

        function ativarLibras(checkbox) {
            const widget = document.querySelector('[vw].enabled');
            widget.style.display = checkbox.checked ? "block" : "none";
            if (checkbox.checked) {
                new window.VLibras.Widget('https://vlibras.gov.br/app');
            }
        }

        function ativarContraste(checkbox) {
            document.body.classList.toggle("dark-mode", checkbox.checked);
            document.querySelector("form").classList.toggle("dark-mode", checkbox.checked);
        }

        function ativarLeitor(checkbox) {
            if (checkbox.checked) {
                alert("Leitor de tela ativado (simulado)");
            }
        }
    </script>
</body>

</html>
