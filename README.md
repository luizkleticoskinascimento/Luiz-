    /* Modo Alto Contraste */
    body.modo-alto-contraste {
        --cor-primaria: #ffff00;
        --cor-secundaria: #00ffff;
        --cor-fundo: #000000;
        --cor-cartao: #121212;
        --cor-texto: #ffffff;
        --cor-destaque: #ff5555;
        --cor-sucesso: #55ff55;
        --cor-alerta: #ffaa00;
    }

    /* ==========================================================
       ESTILOS GERAIS DA PÁGINA
       ========================================================== */
    * {
        box-sizing: border-box;
        margin: 0;
        padding: 0;
        font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    }

    body {
        background-color: var(--cor-fundo);
        color: var(--cor-texto);
        font-size: var(--tamanho-fonte);
        line-height: 1.6;
        transition: background-color 0.3s, color 0.3s;
    }

    .container {
        max-width: var(--largura-maxima);
        margin: 0 auto;
        padding: 0 20px;
    }

    /* ==========================================================
       BARRA DE ACESSIBILIDADE FIXA
       ========================================================== */
    .barra-acessibilidade {
        background-color: var(--cor-primaria);
        color: #ffffff;
        padding: 10px 0;
        border-bottom: 2px solid var(--cor-secundaria);
    }

    .barra-acessibilidade .container {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 10px;
    }

    .controles-acessibilidade {
        display: flex;
        gap: 10px;
        align-items: center;
    }

    .botao-acessibilidade {
        background-color: #ffffff;
        color: #000000;
        border: 2px solid #000000;
        padding: 6px 14px;
        border-radius: 6px;
        font-weight: bold;
        cursor: pointer;
        font-size: 1rem;
        display: inline-flex;
        align-items: center;
        gap: 5px;
    }

    .botao-acessibilidade:hover, .botao-acessibilidade:focus {
        background-color: var(--cor-secundaria);
        color: #000000;
        outline: 3px solid #ffff00;
    }

    /* ==========================================================
       CABEÇALHO E MENU DE NAVEGAÇÃO
       ========================================================== */
    .cabecalho-principal {
        background-color: var(--cor-cartao);
        padding: 20px 0;
        box-shadow: 0 4px 6px rgba(0,0,0,0.1);
        position: sticky;
        top: 0;
        z-index: 100;
    }

    .cabecalho-conteudo {
        display: flex;
        justify-content: space-between;
        align-items: center;
        flex-wrap: wrap;
        gap: 15px;
    }

    .logotipo {
        font-size: 1.8rem;
        font-weight: bold;
        color: var(--cor-primaria);
        display: flex;
        align-items: center;
        gap: 10px;
    }

    body.modo-alto-contraste .logotipo {
        color: var(--cor-primaria);
    }

    .menu-navegacao ul {
        display: flex;
        list-style: none;
        gap: 15px;
        flex-wrap: wrap;
    }

    .menu-navegacao a {
        text-decoration: none;
        color: var(--cor-texto);
        font-weight: bold;
        padding: 8px 12px;
        border-radius: 4px;
        transition: background 0.2s;
    }

    .menu-navegacao a:hover, .menu-navegacao a:focus {
        background-color: var(--cor-secundaria);
        color: #000000;
    }

    /* ==========================================================
       BANNER INICIAL DE BOAS-VINDAS
       ========================================================== */
    .banner-boas-vindas {
        background: linear-gradient(135deg, var(--cor-primaria), #0d2538);
        color: #ffffff;
        padding: 50px 20px;
        text-align: center;
        border-radius: 12px;
        margin: 30px 0;
        box-shadow: 0 4px 12px rgba(0,0,0,0.15);
    }

    body.modo-alto-contraste .banner-boas-vindas {
        background: var(--cor-cartao);
        border: 3px solid var(--cor-primaria);
        color: var(--cor-texto);
    }

    .banner-boas-vindas h1 {
        font-size: 2.3rem;
        margin-bottom: 15px;
    }

    .banner-boas-vindas p {
        font-size: 1.2rem;
        max-width: 800px;
        margin: 0 auto 25px auto;
    }

    .botoes-acao {
        display: flex;
        justify-content: center;
        gap: 15px;
        flex-wrap: wrap;
    }

    .botao-destaque {
        background-color: var(--cor-secundaria);
        color: #000000;
        padding: 14px 28px;
        text-decoration: none;
        font-weight: bold;
        border-radius: 8px;
        font-size: 1.1rem;
        display: inline-block;
        box-shadow: 0 4px 6px rgba(0,0,0,0.2);
    }

    .botao-destaque:hover {
        filter: brightness(1.1);
    }

    /* ==========================================================
       SEÇÕES DE CONTEÚDO E CARTÕES
       ========================================================== */
    .secao-conteudo {
        padding: 40px 0;
        border-bottom: 1px solid #ddd;
    }

    .titulo-secao {
        font-size: 1.9rem;
        color: var(--cor-primaria);
        margin-bottom: 25px;
        display: flex;
        align-items: center;
        gap: 12px;
        border-bottom: 3px solid var(--cor-secundaria);
        padding-bottom: 8px;
    }

    body.modo-alto-contraste .titulo-secao {
        color: var(--cor-primaria);
    }

    .grade-cartoes {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 25px;
    }

    .cartao {
        background-color: var(--cor-cartao);
        border-radius: 10px;
        padding: 25px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.08);
        border: 2px solid transparent;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
    }

    body.modo-alto-contraste .cartao {
        border: 2px solid var(--cor-texto);
    }

    .cartao-alerta {
        border-top: 6px solid var(--cor-destaque);
    }

    .cartao-direito {
        border-top: 6px solid var(--cor-sucesso);
    }

    .cartao-dica {
        border-top: 6px solid var(--cor-secundaria);
    }

    .cartao h3 {
        font-size: 1.4rem;
        margin-bottom: 12px;
        color: var(--cor-primaria);
    }

    body.modo-alto-contraste .cartao h3 {
        color: var(--cor-primaria);
    }

    .tag-alerta {
        background-color: #fee2e2;
        color: #991b1b;
        padding: 4px 8px;
        border-radius: 4px;
        font-size: 0.9rem;
        font-weight: bold;
        display: inline-block;
        margin-bottom: 10px;
    }

    body.modo-alto-contraste .tag-alerta {
        background-color: #ff0000;
        color: #ffffff;
    }

    /* ==========================================================
       LISTA DE CHECKLIST DO DIA A DIA
       ========================================================== */
    .caixa-checklist {
        background-color: var(--cor-cartao);
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.08);
    }

    .item-checklist {
        display: flex;
        align-items: flex-start;
        gap: 15px;
        margin-bottom: 20px;
        padding-bottom: 15px;
        border-bottom: 1px solid #eee;
    }

    .item-checklist input[type="checkbox"] {
        width: 24px;
        height: 24px;
        cursor: pointer;
        margin-top: 3px;
    }

    .texto-checklist h4 {
        font-size: 1.2rem;
        margin-bottom: 4px;
    }

    /* ==========================================================
       QUIZ INTERATIVO (TESTE SEUS CONHECIMENTOS)
       ========================================================== */
    .caixa-quiz {
        background-color: var(--cor-cartao);
        padding: 30px;
        border-radius: 10px;
        box-shadow: 0 4px 8px rgba(0,0,0,0.08);
    }

    .opcao-quiz {
        display: block;
        width: 100%;
        text-align: left;
        background-color: var(--cor-fundo);
        color: var(--cor-texto);
        border: 2px solid #ccc;
        padding: 15px;
        margin: 10px 0;
        border-radius: 8px;
        font-size: 1.1rem;
        cursor: pointer;
    }

    .opcao-quiz:hover {
        border-color: var(--cor-secundaria);
    }

    .mensagem-resultado {
        margin-top: 20px;
        padding: 15px;
        border-radius: 8px;
        font-weight: bold;
        display: none;
    }

    .resultado-correto {
        background-color: #d1e7dd;
        color: #0f5132;
        border: 1px solid #badbcc;
    }

    .resultado-incorreto {
        background-color: #f8d7da;
        color: #842029;
        border: 1px solid #f5c2c7;
    }

    /* ==========================================================
       CONTATOS DE EMERGÊNCIA
       ========================================================== */
    .grade-emergencia {
        display: grid;
        grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
        gap: 20px;
    }

    .cartao-emergencia {
        background-color: var(--cor-cartao);
        padding: 20px;
        text-align: center;
        border-radius: 8px;
        border: 2px dashed var(--cor-destaque);
    }

    .numero-telefone {
        font-size: 2rem;
        font-weight: bold;
        color: var(--cor-destaque);
        margin: 10px 0;
        display: block;
    }

    /* ==========================================================
       RODAPÉ
       ========================================================== */
    .rodape-principal {
        background-color: var(--cor-primaria);
        color: #ffffff;
        padding: 30px 0;
        text-align: center;
        margin-top: 50px;
    }

    body.modo-alto-contraste .rodape-principal {
        background-color: #000000;
        border-top: 3px solid var(--cor-primaria);
    }

    /* Ajuste para telas pequenas */
    @media (max-width: 768px) {
        .cabecalho-conteudo {
            flex-direction: column;
            align-items: flex-start;
        }

        .banner-boas-vindas h1 {
            font-size: 1.8rem;
        }
    }
</style>
