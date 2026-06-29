```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>::: MEU BLOG DE HOMESTUCK ::: NOVO LAYOUT 2009 !!!1!</title>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Press+Start+2P&display=swap" rel="stylesheet">

    <script src="https://cdn.jsdelivr.net/npm/canvas-confetti@1.6.0/dist/confetti.browser.min.js"></script>

    <style>
        /* Configurações Globais e Fundo Estendido d Nuvens */
        body {
            margin: 0;
            padding: 0;
            background-image: url('https://f4.bcbits.com/img/a3224247211_16.jpg');
            background-size: cover;
            background-repeat: repeat;
            background-attachment: fixed;
            background-position: center;
            font-family: 'Press Start 2P', cursive;
            color: #000000;
            font-size: 11px;
            line-height: 1.8;
        }

        /* --- 1. CABEÇALHO DO BLOG --- */
        .blog-header {
            display: block;
            text-align: center;
            padding: 30px 20px;
            background-color: rgba(255, 255, 255, 0.85);
            border-bottom: 6px double #ff0000;
            position: relative;
        }

        .logo-top {
            max-width: 100px;
            height: auto;
            margin: 0 auto 10px auto;
            display: block;
        }

        .blog-title {
            color: #ff0000;
            font-size: 26px;
            margin: 10px 0;
            text-shadow: 4px 4px #e0e0e0;
            letter-spacing: -2px;
        }

        .logo-bottom {
            max-width: 350px;
            width: 100%;
            height: auto;
            margin: 10px auto 0 auto;
            display: block;
        }

        /* --- 2. LAYOUT EM DUAS COLUNAS --- */
        .main-layout {
            max-width: 1000px;
            margin: 30px auto;
            display: flex;
            gap: 20px;
            padding: 0 15px;
        }

        /* Coluna Esquerda: Posts */
        .content-area {
            flex: 2;
        }

        /* Coluna Direita: Barra Lateral */
        .sidebar-area {
            flex: 1;
            display: flex;
            flex-direction: column;
            gap: 20px;
        }

        /* Caixas de Conteúdo */
        .post-container, .widget-container {
            background-color: rgba(255, 255, 255, 0.95);
            border: 3px solid #ff0000;
            box-shadow: 6px 6px 0px #cccccc;
            padding: 20px;
            margin-bottom: 25px;
        }

        .post-title, .widget-title {
            background-color: #efefef;
            padding: 8px;
            border: 2px solid #000;
            margin-top: 0;
            margin-bottom: 20px;
            font-size: 11px;
            color: #000;
            text-align: left;
        }

        /* --- 3. ESTILOS DE TEXTO E PERSONAGENS --- */
        .post-content p {
            margin-bottom: 15px;
            word-wrap: break-word;
        }

        .char-card {
            background-color: rgba(0, 0, 0, 0.05);
            border: 1px dashed #555;
            padding: 12px;
            margin: 15px 0;
        }

        /* Layout Lado a Lado */
        .trolls-section, .kids-section {
            display: flex;
            gap: 20px;
            align-items: flex-start;
        }

        .trolls-text-list, .kids-text-list {
            flex: 1.2;
        }

        .trolls-image-box, .kids-image-box {
            flex: 0.8;
            background-color: #fff;
            border: 3px dashed #ff0000;
            padding: 10px;
            text-align: center;
        }

        .trolls-full-img, .kids-full-img {
            width: 100%;
            height: auto;
            image-rendering: pixelated;
        }

        /* Cores dos Textos */
        .tc-aradia { color: #a10000; }
        .tc-tavros { color: #a15000; }
        .tc-sollux { color: #a1a100; }
        .tc-karkat { color: #ff0000; }
        .tc-nepeta { color: #416600; }
        .tc-kanaya { color: #008141; }
        .tc-terezi { color: #008282; }
        .tc-vriska { color: #005682; }
        .tc-equius { color: #000056; }
        .tc-gamzee { color: #2b0057; }
        .tc-eridan { color: #6a0dad; }
        .tc-feferi { color: #ff007f; }

        .highlight-blue { color: #00b2df; }
        .highlight-pink { color: #ff00ff; }
        .highlight-red { color: #ff0000; }
        .highlight-green { color: #3ab915; }
        .highlight-purple { color: #6a0dad; }

        /* --- 4. MIDIAS E LINKS DO POST --- */
        .image-box {
            background-color: #fff;
            border: 2px solid #ff0000;
            padding: 15px;
            margin: 20px auto;
            display: inline-block;
            text-align: center;
        }

        .karkat-img, .dave-img, .bro-gif {
            max-width: 180px;
            height: auto;
            image-rendering: pixelated;
        }

        .official-link {
            display: block;
            color: #000000;
            background-color: #ffff00;
            padding: 12px;
            text-decoration: none;
            border: 2px solid #000000;
            box-shadow: 4px 4px 0px #000000;
            text-align: center;
            margin: 20px 0;
            font-size: 10px;
        }

        .official-link:hover {
            background-color: #ff0000;
            color: #fff;
        }

        /* --- 5. INTERAÇÕES DA BARRA LATERAL --- */
        .btn-interact {
            display: block;
            width: 100%;
            background-color: #eee;
            color: #ff0000;
            border: 2px solid #ff0000;
            padding: 10px;
            font-family: 'Press Start 2P', cursive;
            font-size: 9px;
            cursor: pointer;
            margin-bottom: 10px;
            box-shadow: 3px 3px 0px #ccc;
            text-align: center;
        }

        .btn-interact:hover {
            background-color: #ff0000;
            color: #fff;
        }

        .status-gif {
            color: #ff3333;
            font-size: 9px;
            text-align: center;
            margin-top: 15px;
        }

        /* Footer GIF Area */
        .footer-gif-container {
            text-align: center;
            padding: 20px;
            margin-top: 20px;
        }

        .footer-gif {
            max-width: 250px;
            height: auto;
            border: 4px ridge #ff0000;
        }

        /* --- 6. EASTER EGG E ANIMAÇÕES --- */
        .hidden-gamzee {
            position: absolute;
            bottom: 8px;
            right: 12px;
            width: 16px;
            height: 16px;
            opacity: 0.15;
            cursor: pointer;
            transition: opacity 0.3s ease, transform 0.2s ease;
            image-rendering: pixelated;
            z-index: 99;
        }

        .hidden-gamzee:hover {
            opacity: 0.85;
            transform: scale(1.3);
        }

        @keyframes sburbShake {
            0% { transform: translate(1px, 1px) rotate(0deg); }
            10% { transform: translate(-1px, -2px) rotate(-1deg); }
            20% { transform: translate(-3px, 0px) rotate(1deg); }
            30% { transform: translate(0px, 2px) rotate(0deg); }
            40% { transform: translate(1px, -1px) rotate(1deg); }
            50% { transform: translate(-1px, 2px) rotate(-1deg); }
            60% { transform: translate(-3px, 1px) rotate(0deg); }
            70% { transform: translate(2px, 1px) rotate(-1deg); }
            80% { transform: translate(-1px, -1px) rotate(1deg); }
            90% { transform: translate(2px, 2px) rotate(0deg); }
            100% { transform: translate(1px, -2px) rotate(-1deg); }
        }

        .homestuck-shake {
            display: inline-block;
        }
        .homestuck-shake:hover {
            animation: sburbShake 0.4s infinite;
        }
    </style>
</head>
<body>

    <header class="blog-header">
        <img class="logo-top" src="https://static.wikia.nocookie.net/mspaintadventures/images/2/2d/Sburb_Logo.svg" alt="Sburb Logo">
        <h1 class="blog-title homestuck-shake">HOMESTUCK BLOG</h1>
        <img class="logo-bottom" src="https://static.wikia.nocookie.net/mspaintadventures/images/a/a7/Homestuck_logo.png" alt="Homestuck Logo">
        
        <img class="hidden-gamzee" id="gamzeeSecret" src="https://images.squarespace-cdn.com/content/v1/5ad21bfa9f4970c995f00e96/1524003290623-WMA45I7Z9LNSUT8O733S/icon_gamzee.png" alt="???" title="Honk!">
    </header>

    <div class="main-layout">
       
        <main class="content-area">
           
            <article class="post-container">
                <h2 class="post-title homestuck-shake">POSTED: 24/10/2009 ==&gt; INFOS GERAIS!!!</h2>
                <div class="post-content">
                    <p>MEU DEUS DO CEU!!!! vc nao ta entendendo!!!!! 8D 8D</p>
                    <p>tipo... vc PRECISA conhecer essa webcomic q ta todo mundo comentando na internet!!!! o nome eh HOMESTUCK e eh do msm cara q fez Jailbreak e Problem Sleuth (o andrew hussie, vulgo mestre supremo kkkk)!!!!</p>
                    <p>eh basicamente a historia d um mlk de 13 anos chamado <span class="highlight-blue">John Egbert</span> (ele curte uns filmes mt ruins d terror e magica kk bem nerd) q ta trancado no quarto esperando um jogo d computador mt foda e misterioso sair em versao Beta... o nome do jogo eh <strong>Sburb</strong>!!!!</p>
                    <p>so q qnd ele e os amigos dele da internet (a <span class="highlight-pink">Rose</span>, o <span class="highlight-red">Dave</span> e a <span class="highlight-green">Jade</span>) comecam a jogar... o jogo simplesmente INTERAGE WITH A REALIDADE!!!! O_O tipo... eles conseguem mover os moveis do quarto uns dos outros usando o mouse do PC!!! mto bizarro dorgas mano kkkkkk</p>
                   
                    <a href="https://www.homestuck.com" target="_blank" class="official-link">
                        ==&gt; CLIQUE AKI PRO SITE OFICIAL DA COMIC !!!!
                    </a>
                </div>
            </article>

            <article class="post-container">
                <h2 class="post-title homestuck-shake">POSTED: 28/10/2009 ==&gt; OS TROLLS CHEGARAM!!!!</h2>
                <div class="post-content">
                    <p>NOOOOSSA kra vc nao ta entendendo o nível da loucura q virou essa parada dps q os TROLLS apareceram!!!! 8D KKKKKKK</p>
                    <p>Eles sao uns alienigenas cinzas de um planeta chamado Alternia, tem chifres de doce, sangue de cores diferentes e ficam trollando os kids pelo Pesterchum!!! Saca so os mais marcantes:</p>
                   
                    <div class="char-card">
                        <span class="highlight-red">KARKAT VANTAS (carcanguejo kk):</span>
                        <p>MEEEU DEUS o bicho eh uma maquina d xingamento!!!! xD ele digita TUDO EM CAPS LOCK E PARECE Q TA SEMPRE GRITANDO COM VOCE!!! ele eh o lider e o sangue dele eh mutante mas ele esconde d todo mundo pra nao morrer... mt tsundere ele!!!! O_O</p>
                       
                        <div class="image-box">
                            <img class="karkat-img" src="https://static.wikia.nocookie.net/mspaintadventures/images/1/17/Karkat_Vantas.png" alt="Karkat">
                        </div>
                    </div>

                    <div class="char-card">
                        <span class="highlight-purple">ERIDAN AMPORA:</span>
                        <p>mano kkkkk o eridan eh mt patetico namoral!!! ele eh da realeza dos trolls (um seadweller) entao ele se acha SUPERIOR A TODO MUNDO. usa uma capa roxa estilosa e usa um quirk onde DUPLICA AS LETRAS "W" E "V" (tipo "wwhat are vyou doing")!!!</p>
                    </div>
                </div>
            </article>

            <article class="post-container">
                <h2 class="post-title homestuck-shake">POSTED: 30/10/2009 ==&gt; GUIA DOS TROLLS!!!1! FICOU MT TENSO XD</h2>
                <div class="post-content">
                    <p>Ow galere resolvi cria esse post especial pa explica de um jeito resumidu kem eh kem nesa rassa de chifrudo d alternia kkk x_x fika vendo o textao q escrevi e a img com todos eles do lado!!!</p>
                    
                    <div class="trolls-section">
                        
                        <div class="trolls-text-list">
                            <p><span class="tc-aradia">ARADIA:</span> a minina fantasma bizarra o_O ela fika flando d morte dpois vira um robo e dpois vira fada lol eli troca as letra "o" por "0" pq e mei morta e sem sentimentus de comesso :P</p>
                            
                            <p><span class="tc-tavros">TAVROS:</span> o mlk manso d chifrao d touro q usa cadera d rodas pq a vriska fudeu as costa deli kkk :-( eli ama uns bixo voador fantasiado e digita INVERTENDU AS MAIUSCULA tIPO aSSIM mANO,</p>
                            
                            <p><span class="tc-sollux">SOLLUX:</span> u radker do grupo!! tem 4 oio de cores difetente (2 azul e 2 vermei) e fala ingasgado kkkk eli digita tdu botando u numero "2" nas palavra pq eli curte binarismo e duplisidade B-)</p>
                            
                            <p><span class="tc-karkat">KARKAT:</span> u cara mas estressado da internet toda!!!1! eli odeia tudu e fik digitando TUDO EM CAPS LOCK GRITANDO COMSIGO MESMO kkkk &gt;:O u sangue deli e vermelho mutante mas e segredo kkk tsundere total</p>
                            
                            <p><span class="tc-nepeta">NEPETA:</span> a otaku dos gatinhu :33 ela mora numa caverna fasendo uns roleplay d caçadora mto dorgas e fica xipando todo mundo nu mural dela!! comesa as frase cum :33 e bota trocadinho d gato kkk mto fofis</p>
                            
                            <p><span class="tc-kanaya">KANAYA:</span> a troll mas xiq estilosa, curte costura, moda e vira um vampiro q brilha nu escuro (rainbow drinker mds kkk) ela DIGITA COMEÇANDO TODA PALAVRA COM MAIUSCULA PRA PARECER CHIQUE!!!</p>
                            
                            <p><span class="tc-terezi">TEREZI:</span> a mina sega mto loca q xera e lambe a tela pra ver as cores kkkk xD ela gosta d dragao, usa oclinhos vermelho e digita cum numeros d led tipu 43551M mto nerd hackeadora d lan house</p>
                            
                            <p><span class="tc-vriska">VRISKA:</span> a pirada dos 8 oio e dos dado magico de RPG :::;) ela e ultra crueeel e fudeu a vida d metade dos amigo kkkk ela vive trocando as letra ou a silaba "oito" pelo num 8 mto chata mas amo ela lol</p>
                            
                            <p><span class="tc-equius">EQUIUS:</span> u monstro fortão eskesito d+ o_o" eli quebra tudo q toca sem querer pq e forte pakarai e fica suando baldes!!! eli gosta d cavalo e comesa os texto botando uma seta d arco D-&gt; pras palavra</p>
                            
                            <p><span class="tc-gamzee">GAMZEE:</span> u troll palhaço do capeta :o) eli fika comendo torta de sopor slime e fika locasso flando d milagres e de deus kkk eli escreve AlTeRnAnDo MaIuScUlA e MiNuScUlA mO rUfIãO dE lEr mds do ceu kkkk</p>
                            
                            <p><span class="tc-eridan">ERIDAN:</span> u troll da rialesa dos mar q se axa superior mas e mó otario patetico kkk kkk eli usa capa e cachecol e odeia os troll d terra querendo matar td mundo. eli bota duas letra "w" e "v" tdu junto :/</p>
                            
                            <p><span class="tc-feferi">FEFERI:</span> a princesa herdera peixe ultra fofinha e animada!! )( ela ama as balea e quer q todo mundo se de bem sem preconceito d casta! ela bota os h maiusculo tipu ) ( e fas cara d peixe nos emoticon -*</p>
                        </div>
                        
                        <div class="trolls-image-box">
                            <p style="color:#ff0000; font-size:9px; margin-bottom:10px;">[ FOTO DA BANCA TODA UNIDA 8D ]</p>
                            <img class="trolls-full-img" src="https://preview.redd.it/rank-the-trolls-from-worst-to-best-in-the-comments-heres-my-v0-qjzlfq8e3btf1.jpeg?auto=webp&s=e30e83a6f8666a2f04c3d1714949a124f1597058" alt="Todos os 12 Trolls de Homestuck Juntos">
                            <p style="font-size:8px; color:#777; margin-top:8px;">olha os doze junto no ranking da net kkkkk o gamzee la atras rindo mds medinho kkkkk</p>
                        </div>
                        
                    </div>
                </div>
            </article>

            <article class="post-container">
                <h2 class="post-title homestuck-shake">POSTED: 02/11/2009 ==&gt; QUEM SÃO AS BETA KIDS?! DETONADO COMPLETO kkkk</h2>
                <div class="post-content">
                    <p>gAlErEeEe!!! fiz esse post super foda pra fofocar e esplicar sobre os 4 humanos principais da comic (as beta kids originais pq eles jogam a versao beta de sburb kkk)!!!! da uma olhada no textao ressumido dorgas mano kkk:</p>
                    
                    <div class="kids-section">
                        <div class="kids-text-list">
                            <p><span class="highlight-blue">JOHN EGBERT:</span> u lider brincalhão do grupo :B ele adora piadas ruins, magicas de salao e eh viciado em filmes trash (tipo con air e nicolas cage kk mto tosco). ele eh super gente boa mas meio lerdo x_x</p>
                            
                            <p><span class="highlight-pink">ROSE LALONDE:</span> a mina gótica intelectual q gosta d ler livros gigantes de terror e tecer cachecol kkkk &gt;:D ela escreve de um jeito todo formal e chique pra caramba e dpois vira um bruxa mto loka das trevas (grimdark mds q medo)!!!</p>
                            
                            <p><span class="highlight-red">DAVE STRIDER:</span> u dj super cool das rimas rapidas d rap B-) ele eh ironico 24 horas por dia e nunca tira os oclinhos de sol nem fodendo!!! ele coleciona coisas mortas e espadas e nao bota nenhuma pontuaçao nos textos kkkk</p>
                            
                            <p><span class="highlight-green">JADE HARLEY:</span> a garota cientista q mora numa ilha deserta com o cachorro gigante dela chamado becquerel!!! :Q ela tem narcolepsia e dorme do nada, adora plantas e usa um rifle gigante pra atirar em monstros mto foda!!!!</p>
                        </div>
                        
                        <div class="kids-image-box">
                            <p style="color:#ff0000; font-size:9px; margin-bottom:10px;">[ OS QUATRO UNIDOS NO SBURB !! ]</p>
                            <img class="kids-full-img" src="https://i.redd.it/beta-kids-my-designs-v0-5eynj1fju9id1.jpg?width=3238&format=pjpg&auto=webp&s=4ccf024ef1ab332621cc256d317586d42dd9be76" alt="Beta Kids Homestuck">
                            <p style="font-size:8px; color:#777; margin-top:8px;">olha os 4 juntos prontos pra quebrar tudo na sessao do jogo!!! 8D</p>
                        </div>
                    </div>
                </div>
            </article>

            <article class="post-container">
                <h2 class="post-title homestuck-shake">POSTED: 01/11/2009 ==&gt; BONUS: O HUMANO MAIS COOL DA INTERNET B-)</h2>
                <div class="post-content">
                    <div class="char-card">
                        <span class="highlight-red">DAVE STRIDER (u DJ dos takos d ironia kkk):</span>
                        <p>MANO kkk o dave eh mto ironico tipu ele NUNCA tira os oclos escuro nem pa dormi kkk B-) ele mora no texas com o Brother dele q e mto pirado e tem fetiche por boneco de ventriloco bizarro e espadas katana x__x</p>
                        <p>o dave faz umas rimas de rap mto rapidas e lokas na internet e o pesterchum dele eh turntechGodhead!!! ele digita TUDO EM MINUSCULO SEM NENHUMA PONTUAÇAO pq ele eh cool dmais pra se importa com a gramatica kkkkk "i am the knight of time" mto foda bixo!!!1!</p>
                        
                        <div class="image-box">
                            <img class="dave-img" src="https://static.wikia.nocookie.net/mspaintadventures/images/e/ee/Dave_Strider.png" alt="Dave Strider">
                        </div>
                        <p style="font-size:9px; text-align:center; color:#555;">olha o estilo do garoto tocando as pick-up mds kkkk mto descolado xD</p>
                    </div>
                </div>
            </article>

            <article class="post-container">
                <h2 class="post-title homestuck-shake">!!! UPDATE TOTALMENTE FINO: OS GUARDS / PROTETORES DA GALERA!! !!!</h2>
                
                <div class="post-content">
                    <p>genteee dpois de falar do mestre das rimas dave strider nois n pode fikar sem falar de kem cuida dssa glr!!! ou tenta né kkkkkk vo posta aki a foto secreta dles q axei perdida num forum bem obscuro flw xd</p>
                    
                    <div class="image-box">
                        <img src="https://share.google/CTyo3IngpFy9eBjVb" alt="Os Protetores brabos" class="kids-full-img">
                        <p>▲ OS COROAS Q MANDAM NO PEDAÇO!!! ▲</p>
                    </div>

                    <hr style="border: 1px dashed #ff0000; margin: 20px 0;">

                    <p>separa ae q cada um tem seu responsavel bem bizarro kkkk se liga nas cores de cada um pra n se perder:</p>

                    <div class="char-card">
                        <p><span class="highlight-blue">**[PAI EGBERT]**</span> o kra eh LITERALMENTE vidrado em tortas e akeles palhaços super assustadores??¿¿ mt eskesito mano!! msm assim o quarto dele eh xeio dsses boneco medonho mas ele eh moh bom pai e fika dando uns presente pro john (pena q o john axa mto paia as coisa kkkkkk) sempre usa terno e gravata msm dentro d ksa!!</p>
                    </div>

                    <div class="char-card">
                        <p><span class="highlight-pink">**[MÃE LALONDE]**</span> a mae da rose eh mó fina, rica e vive bebendo uns drink maluko numa taça o dia todo... a relaçao dlas eh pura ironia e mto passivo-agressiva kkkkk se comunicam por puro sarcasmo e uns papo d mago das trevas e magias ocultas!! 0_0</p>
                    </div>

                    <div class="char-card">
                        <p><span class="highlight-green">**[VOVÔ HARLEY]**</span> o vovo ja faleceu mas ele era um p*ta explorador brabo d+ q empalhou um monte de bixo esquisito na ksa dela na ilha!! dexa o Becquerel (o dog com poders espaciais mt apelao) tomando conta de tdo pra ela n fikar sozinha!!</p>
                    </div>

                    <hr style="border: 1px dashed #ff0000; margin: 20px 0;">

                    <blockquote style="background-color: #efefef; border: 3px solid #ff0000; padding: 15px; margin: 20px 0; box-shadow: 4px 4px 0px #cccccc;">
                        <h3 class="homestuck-shake" style="color: #ff0000; margin-top: 0; font-size: 11px; text-align: center;">B-) O CARA MAIS MEGA ULTRA SUPREMO E IRADO DA INTERNET: BRO STRIDER!!! ⟵⁠(⁠o⁠_⁠O⁠)</h3>
                        
                        <p>pqp glr agr papo serio de verdade aki.... o q eh o protetor do <span class="highlight-red">**Dave**</span>???? o lendario **BRO STRIDER** eh simplemente o auge do estilo, do SWAG total e da ironia moderna!!!!! B)</p>
                        
                        <p>o kra vive com akeles oculos escuros pontudos icónicos que NUNCA SAEM DO ROSTO nem fud*ndo!! ele eh um DJ profissional super foda, faz umas batalha de rima com ironia suprema e coleciona uns boneco de ventriloco mt bizarro (os lendarios Cal Puppets) so de zueira pela pura ironia kkkkkkk</p>
                        
                        <p>e o mais insano de tudo: o kra treina o dave fazendo **BATALHA DE ESPADA NINJA REAL NO TETO DO APARTAMENTO** la em houston, texas!!! isso msm o kra corre tanto q desafia as lei da gravidade bixo!!! nao tem absolutamente NINGUEM mais descolado, frio, calculista e maneiro na blogosfera inteira q o Bro. o cara exala a pura essencia dos anos 2000 mt mitologico, impossivel n axar ele fodastico!!!!! $滑</p>
                        
                        <div class="image-box">
                            <img class="bro-gif" src="https://media2.giphy.com/media/v1.Y2lkPTZjMDliOTUyaWkxYXMwN3NwNXAxdms1b2d0MnBuM3Fmcjg2MjQwNGN5azc5NW56ZyZlcD12MV9naWZzX3NlYXJjaCZjdD1n/bGBPJbo4PGoZjvFQQP/200.gif" alt="Bro Strider Gif">
                        </div>
                    </blockquote>

                </div>
            </article>

            <article class="post-container">
                <h2 class="post-title homestuck-shake">POSTED: 25/10/2009 ==&gt; MINHAS TEORIAS LOCAS E SHIPS!!!1! XD </h2>
                <div class="post-content">
                    <p>Oww galera!!! dpois d fla do Bro ontem fikei ate de madruga lendo a comic de nv e mtas ideia ferraram minha cabeça kkkk @_@ prsisa mto bota as teoria e meus casal fofis aki!!</p>
                    
                    <div class="char-card">
                        <p style="color: #6a0dad;">(⁠・⁠o⁠・⁠) TEORIA CONSPIRATORIA DO MAL:</p>
                        <p>mano e se o jogo <span class="highlight-purple">Sburb</span> n for soh um jogo mas tipu... uma parada d criar universos?? kkk moh dorgas mano @_@ axo q o mundo vai acaba d vdd na comic e eles vao te q vira deuses!! anotem ae dpois n flão q n avisei!!1!</p>
                    </div>

                    <div class="char-card">
                        <p style="color: #ff00ff;">♡ MEUS SHIPS FAVORITUS (NÃO ME JULGEM KKK):</p>
                        <p>1. <span class="highlight-blue">John</span> x <span class="highlight-pink">Terezi</span>: mto bunitu eles flando d nerdise!! msm ela sndo mei loka e ele mei bobao axo q combinan d+!! :3</p>
                        <p>2. <span class="highlight-red">Dave</span> x <span class="highlight-green">Karkat</span>: o kra todo ironico d oclinhos e o kra todu revoltado kkkk o oposto se atrae total bixo!! mto fofis s2 B-)</p>
                        <p>3. <span class="highlight-red">Equius</span> x <span class="highlight-blue">Nepeta</span>: kkkk brinks... ou nao??? imagina a nepeta arranhando o Equius e rindo da cara delekkkk ia se mto comedia xD XD</p>
                    </div>
                    
                    <p>oq vcs axam dsses bglh?? comentem ae em baxo c vcs axam q faz sentido ou c usei mta slimea de troll kkkkkk xD XD</p>
                </div>
            </article>

        </main>

        <aside class="sidebar-area">
           
            <div class="widget-container">
                <h3 class="widget-title">INTERAÇÕES DOS FÃS</h3>
                <button class="btn-interact" onclick="alert('Vc curtiu esse post! XD')">[ CURTIR POST ]</button>
                <button class="btn-interact" onclick="alert('Função de comentários abrirá no MSN kkkk brinks')">[ COMENTAR ]</button>
                <button class="btn-interact" onclick="alert('Adicionado aos favoritos do seu Internet Explorer!')">[ FAVORITAR ]</button>
            </div>

            <div class="widget-container">
                <h3 class="widget-title">MY STATUS</h3>
                <p>Ouvindo: Midnight Crew MIDI Track</p>
                <p>Navegador: Firefox 3.5</p>
                <div class="status-gif">
                    [ NET DISCADA: ONLINE ] <br>
                    !!!1!1!!1!!
                </div>
            </div>

        </aside>

    </div>

    <div class="footer-gif-container">
        <img class="footer-gif" src="https://img1.picmix.com/output/pic/normal/6/4/0/6/13006046_26459.gif" alt="Homestuck Troll Animation">
        <p style="font-family: 'Press Start 2P', cursive; font-size: 8px; color: #ffffff; text-shadow: 2px 2px #000; margin-top: 10px;">::: FIM DA PAGINA !!! VOLTE SEMPRE !!! 8D :::</p>
    </div>

    <script>
        document.getElementById('gamzeeSecret').addEventListener('click', function() {
            const bloodCastes = ['#2b0057', '#ff0000', '#008282', '#416600', '#a1a100', '#ff007f'];
            
            confetti({
                particleCount: 75,
                angle: 60,
                spread: 60,
                origin: { x: 0, y: 0.8 },
                colors: bloodCastes
            });
            
            confetti({
                particleCount: 75,
                angle: 120,
                spread: 60,
                origin: { x: 1, y: 0.8 },
                colors: bloodCastes
            });
        });
    </script>

</body>
</html>

```
