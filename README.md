# Assinatura<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Fã-Clube VIP - Comunidade & Curso de Desenho</title>
    <style>
        :root {
            --bg-color: #0f0f13;
            --card-bg: #1a1a24;
            --primary: #8a2be2;
            --secondary: #ff477e;
            --accent: #ffd166;
            --text-main: #f8f9fa;
            --text-muted: #a0a0b8;
            --success: #06d6a0;
            
            /* Cores das Redes */
            --instagram: linear-gradient(45deg, #f9ce34, #ee2a7b, #6228d7);
            --youtube: #ff0000;
            --tiktok: #000000;
            --twitch: #9146ff;
            --discord: #5865f2;
            --livepix: #00ffaa;
        }

        * {
            box-sizing: border-box;
            margin: 0;
            padding: 0;
            font-family: 'Segoe UI', Roboto, Helvetica, Arial, sans-serif;
        }

        body {
            background-color: var(--bg-color);
            color: var(--text-main);
            line-height: 1.6;
        }

        header {
            background: linear-gradient(135deg, #1e1233 0%, #0f0f13 100%);
            padding: 60px 20px;
            text-align: center;
            border-bottom: 2px solid #242433;
            position: relative;
            overflow: hidden;
        }

        header::before {
            content: '';
            position: absolute;
            top: -50%;
            left: -50%;
            width: 200%;
            height: 200%;
            background: radial-gradient(circle, rgba(138,43,226,0.15) 0%, transparent 60%);
            z-index: 1;
        }

        .header-container {
            position: relative;
            z-index: 2;
            max-width: 800px;
            margin: 0 auto;
        }

        header h1 {
            font-size: 3rem;
            color: var(--text-main);
            margin-bottom: 15px;
            letter-spacing: -1px;
        }

        header h1 span {
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }

        header p {
            font-size: 1.2rem;
            color: var(--text-muted);
            max-width: 600px;
            margin: 0 auto 30px auto;
        }

        .buttons-group {
            display: flex;
            justify-content: center;
            gap: 15px;
            flex-wrap: wrap;
        }

        .cta-btn {
            display: inline-block;
            background: linear-gradient(45deg, var(--primary), var(--secondary));
            color: white;
            padding: 14px 30px;
            border-radius: 50px;
            text-decoration: none;
            font-weight: bold;
            font-size: 1.1rem;
            box-shadow: 0 4px 15px rgba(138,43,226,0.4);
            transition: transform 0.2s, box-shadow 0.2s;
            border: none;
            cursor: pointer;
        }

        .cta-btn:hover {
            transform: translateY(-2px);
            box-shadow: 0 6px 20px rgba(138,43,226,0.6);
        }

        main {
            max-width: 1100px;
            margin: 40px auto;
            padding: 0 20px;
        }

        .section-title {
            text-align: center;
            font-size: 2rem;
            margin-bottom: 40px;
            position: relative;
        }

        .section-title::after {
            content: '';
            display: block;
            width: 60px;
            height: 4px;
            background: var(--secondary);
            margin: 10px auto 0 auto;
            border-radius: 2px;
        }

        /* Grid de Planos e Benefícios */
        .grid-container {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(250px, 1fr)); /* Ajustado para caber 4 cards melhor */
            gap: 30px;
            margin-bottom: 60px;
        }

        .card {
            background-color: var(--card-bg);
            border: 1px solid #242433;
            border-radius: 16px;
            padding: 35px;
            display: flex;
            flex-direction: column;
            justify-content: space-between;
            position: relative;
            transition: transform 0.3s, border-color 0.3s;
        }

        .card:hover {
            transform: translateY(-5px);
            border-color: var(--primary);
        }

        .card.featured {
            border: 2px solid var(--secondary);
        }

        .badge {
            position: absolute;
            top: 15px;
            right: 15px;
            background-color: var(--secondary);
            color: white;
            font-size: 0.8rem;
            padding: 4px 12px;
            border-radius: 20px;
            font-weight: bold;
        }

        .card h3 {
            font-size: 1.5rem;
            margin-bottom: 15px;
        }

        .price {
            font-size: 2.2rem;
            font-weight: 800;
            color: var(--text-main);
            margin-bottom: 20px;
            display: flex;
            align-items: baseline;
            flex-wrap: wrap;
        }

        .price span {
            font-size: 0.9rem;
            color: var(--text-muted);
            font-weight: normal;
            margin-left: 5px;
        }

        .features-list {
            list-style: none;
            margin-bottom: 30px;
        }

        .features-list li {
            margin-bottom: 12px;
            display: flex;
            align-items: center;
            color: var(--text-muted);
            font-size: 0.9rem;
        }

        .features-list li::before {
            content: '✓';
            color: var(--success);
            font-weight: bold;
            margin-right: 10px;
            font-size: 1.1rem;
        }

        /* Seção do Curso de Desenho */
        .course-section {
            background: linear-gradient(135deg, #1a1a24 0%, #15151e 100%);
            border: 1px solid #242433;
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 60px;
        }

        .course-header {
            display: flex;
            align-items: center;
            justify-content: space-between;
            flex-wrap: wrap;
            gap: 20px;
            margin-bottom: 30px;
            border-bottom: 1px solid #242433;
            padding-bottom: 20px;
        }

        .course-badge {
            background-color: var(--success);
            color: #000;
            font-weight: bold;
            padding: 6px 16px;
            border-radius: 4px;
            text-transform: uppercase;
            font-size: 0.9rem;
        }

        .modules-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
            gap: 20px;
        }

        .module-item {
            background-color: #222230;
            padding: 20px;
            border-radius: 10px;
            border-left: 4px solid var(--primary);
        }

        .module-item h4 {
            margin-bottom: 8px;
            color: var(--accent);
        }

        .module-item p {
            font-size: 0.9rem;
            color: var(--text-muted);
        }

        /* Nova Seção de Redes Sociais */
        .social-section {
            background-color: var(--card-bg);
            border: 1px solid #242433;
            border-radius: 20px;
            padding: 40px;
            margin-bottom: 60px;
        }

        .social-grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(160px, 1fr));
            gap: 15px;
            margin-top: 20px;
        }

        .social-btn {
            display: flex;
            align-items: center;
            justify-content: center;
            padding: 12px;
            border-radius: 8px;
            color: white;
            text-decoration: none;
            font-weight: bold;
            font-size: 0.95rem;
            transition: transform 0.2s, opacity 0.2s;
            text-align: center;
        }

        .social-btn:hover {
            transform: scale(1.03);
            opacity: 0.9;
        }

        .btn-instagram { background: var(--instagram); }
        .btn-youtube { background-color: var(--youtube); }
        .btn-tiktok { background-color: var(--tiktok); border: 1px solid #333; }
        .btn-twitch { background-color: var(--twitch); }
        .btn-discord { background-color: var(--discord); }

        /* Seção de Pagamento PIX e Livepix */
        .pix-section {
            background-color: #121216;
            border: 2px dashed #343444;
            border-radius: 20px;
            padding: 40px;
            text-align: center;
            max-width: 600px;
            margin: 0 auto;
        }

        .pix-title {
            color: var(--success);
            font-size: 1.5rem;
            margin-bottom: 15px;
            display: flex;
            align-items: center;
            justify-content: center;
            gap: 10px;
        }

        .pix-key-box {
            background-color: #1e1e26;
            padding: 15px;
            border-radius: 10px;
            font-family: monospace;
            font-size: 1.3rem;
            color: var(--accent);
            margin: 20px 0;
            border: 1px solid #2d2d3d;
            word-break: break-all;
            user-select: all;
            cursor: pointer;
        }

        .pix-instruction {
            font-size: 0.95rem;
            color: var(--text-muted);
            margin-bottom: 10px;
        }

        .btn-livepix {
            background: linear-gradient(45deg, #00f2fe, #4facfe);
            color: #000;
            margin-top: 20px;
            width: 100%;
            text-align: center;
            box-shadow: 0 4px 15px rgba(0, 242, 254, 0.3);
        }

        .btn-livepix:hover {
            box-shadow: 0 6px 20px rgba(0, 242, 254, 0.5);
        }

        .email-link {
            color: var(--secondary);
            text-decoration: none;
            font-weight: bold;
            border-bottom: 1px dashed var(--secondary);
            transition: color 0.2s;
        }

        .email-link:hover {
            color: var(--accent);
            border-bottom-color: var(--accent);
        }

        footer {
            text-align: center;
            padding: 40px 20px;
            margin-top: 8px;
            color: var(--text-muted);
            border-top: 1px solid #242433;
            font-size: 0.9rem;
        }

        @media (max-width: 768px) {
            header h1 { font-size: 2.2rem; }
            .course-header { flex-direction: column; text-align: center; }
            .buttons-group { flex-direction: column; align-items: center; }
            .cta-btn { width: 100%; text-align: center; }
        }
    </style>
</head>
<body>

    <header>
        <div class="header-container">
            <h1>Fã-Clube <span>VIP Oficial</span></h1>
            <p>Faça parte da nossa comunidade exclusiva, ganhe vantagens incríveis para interagir nos vídeos e domine a arte do desenho sem pagar nada por isso!</p>
            <div class="buttons-group">
                <a href="#planos" class="cta-btn">Ver Planos de Acesso</a>
                <a href="#redes" class="cta-btn" style="background: #242433; border: 1px solid var(--text-muted);">Nossos Canais</a>
            </div>
        </div>
    </header>

    <main>
        
        <section class="course-section">
            <div class="course-header">
                <div>
                    <h2>Curso de Desenho Completo</h2>
                    <p style="color: var(--text-muted); margin-top: 5px;">Aprenda do zero de forma simples e prática</p>
                </div>
                <span class="course-badge">100% Grátis</span>
            </div>
            
            <div class="modules-grid">
                <div class="module-item">
                    <h4>Módulo 1: Traços Iniciais</h4>
                    <p>Como dominar a coordenação motora e fazer formas perfeitas de um jeito simples.</p>
                </div>
                <div class="module-item">
                    <h4>Módulo 2: Luz e Sombra</h4>
                    <p>Descubra o segredo do sombreamento realista para dar volume aos seus desenhos.</p>
                </div>
                <div class="module-item">
                    <h4>Módulo 3: Personagens</h4>
                    <p>Passo a passo descomplicado para desenhar rostos e corpos na proporção certa.</p>
                </div>
            </div>
        </section>

        <section id="redes" class="social-section">
            <h2 class="section-title">Nossas Redes Oficiais</h2>
            <p style="text-align: center; color: var(--text-muted); margin-top: -20px;">Siga e interaja em todas as plataformas para não perder nenhum conteúdo!</p>
            
            <div class="social-grid">
                <a href="https://www.instagram.com/matheus_wandscher_?igsh=MWZ5aHk3OTgybWh5Yw==" target="_blank" class="social-btn btn-instagram">Instagram</a>
                <a href="https://youtube.com/@mt_wandscher?si=ZOrfsn49cuw2niXO" target="_blank" class="social-btn btn-youtube">YouTube</a>
                <a href="https://www.tiktok.com/@mt_wandscher?_r=1&_t=ZS-969Po0x8yRg" target="_blank" class="social-btn btn-tiktok">TikTok</a>
                <a href="https://twitch.com/mt_wandscher" target="_blank" class="social-btn btn-twitch">Twitch</a>
                <a href="https://discord.gg/7JU5zDvC8" target="_blank" class="social-btn btn-discord">Discord</a>
            </div>
        </section>

        <section id="planos">
            <h2 class="section-title">Escolha Seu Nível de Apoio</h2>
            
            <div class="grid-container">
                
                <div class="card">
                    <div>
                        <h3>Assinatura do Desenho</h3>
                        <div class="price">R$ 5,68<span>/mês</span></div>
                        <ul class="features-list">
                            <li>Conteúdo extra de desenho</li>
                            <li>Acesso aos rascunhos originais</li>
                            <li>Dicas exclusivas de arte</li>
                        </ul>
                    </div>
                    <a href="#pagamento" class="cta-btn" style="background: #242433; border: 1px solid var(--accent); text-align: center;">Apoiar com Arte</a>
                </div>

                <div class="card">
                    <div>
                        <h3>Pacote Figurinhas VIP</h3>
                        <div class="price">R$ 15,25<span>/taxa única</span></div>
                        <ul class="features-list">
                            <li>Figurinhas personalizadas exclusivas</li>
                            <li>Destaque em vídeos do canal</li>
                            <li>Uso liberado nos comentários</li>
                            <li>Acesso ao grupo de apoiadores</li>
                        </ul>
                    </div>
                    <a href="#pagamento" class="cta-btn" style="background: #242433; border: 1px solid var(--primary); text-align: center;">Liberar Agora</a>
                </div>

                <div class="card featured">
                    <span class="badge">Mais Vendido</span>
                    <div>
                        <h3>Assinatura Mensal</h3>
                        <div class="price">R$ 12,90<span>/mês</span></div>
                        <ul class="features-list">
                            <li>Todos os benefícios de figurinhas</li>
                            <li>Interação prioritária em comentários</li>
                            <li>Participação em enquetes de vídeos</li>
                            <li>Acesso antecipado aos conteúdos</li>
                        </ul>
                    </div>
                    <a href="#pagamento" class="cta-btn" style="text-align: center;">Assinar Mensal</a>
                </div>

                <div class="card">
                    <div>
                        <h3>Plano Anual Premium</h3>
                        <div class="price">R$ 100,00<span>/ano</span></div>
                        <ul class="features-list">
                            <li>Economia de mais de R$ 54,00</li>
                            <li>Acesso completo por 12 meses</li>
                            <li>Todos os benefícios inclusos</li>
                            <li>Selo VIP permanente no perfil</li>
                        </ul>
                    </div>
                    <a href="#pagamento" class="cta-btn" style="background: #242433; border: 1px solid var(--secondary); text-align: center;">Garantir Plano Anual</a>
                </div>

            </div>
        </section>

        <section id="pagamento" class="pix-section">
            <h3 class="pix-title">
                <svg width="24" height="24" viewBox="0 0 24 24" fill="none" xmlns="http://www.w3.org/2000/svg" style="vertical-align: middle;">
                    <path d="M12 2L2 12L12 22L22 12L12 2ZM4.83 12L12 4.83L19.17 12L12 19.17L4.83 12Z" fill="#06d6a0"/>
                    <path d="M12 8L8 12L12 16L16 12L12 8Z" fill="#06d6a0"/>
                </svg>
                Formas de Pagamento
            </h3>
            <p class="pix-instruction">Transfira o valor exato do plano escolhido diretamente para a nossa chave PIX:</p>
            
            <div class="pix-key-box" title="Clique para selecionar">15998015908</div>
            
            <p class="pix-instruction">Ou prefere pagar direto por plataforma? Use o link automático abaixo:</p>
            <a href="https://livepix.gg/mtwandscher" target="_blank" class="cta-btn btn-livepix">Apoiar via Livepix (Cartão/PIX)</a>
            
            <p class="pix-instruction" style="font-size: 0.85rem; margin-top: 25px;">
                💡 <strong>Dica Importante:</strong> Após realizar o pagamento por PIX ou Livepix, envie o comprovante para o nosso e-mail: <a href="mailto:matheuswandscher11@gmail.com" class="email-link">matheuswandscher11@gmail.com</a> para adicionarmos você ao grupo e liberarmos as suas recompensas!
            </p>
        </section>

    </main>

    <footer>
        <p>&copy; 2026 Fã-Clube Oficial. Todos os direitos reservados.</p>
    </footer>

</body>
</html>