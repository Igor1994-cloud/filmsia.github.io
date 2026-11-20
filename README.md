# IAFlix — site de vídeos com IA

Projeto front-end feito com HTML, CSS e JavaScript puro.

## Como executar
1. Extraia a pasta `iaflix_site`.
2. Abra `index.html` no navegador.
3. Para desenvolvimento, você também pode abrir a pasta no VS Code e usar a extensão Live Server.

## Estrutura
- `index.html` — estrutura e páginas.
- `css/style.css` — visual responsivo.
- `js/app.js` — vídeos demonstrativos, busca, gêneros, player e perfil.

## Como colocar seus vídeos
No início de `js/app.js`, cada vídeo possui a propriedade `url`. Coloque nela o endereço direto de um arquivo de vídeo MP4, por exemplo:
`url: "videos/minha-historia.mp4"`
Crie a pasta `videos` e coloque o arquivo nela. Para vídeos hospedados, use uma URL direta que permita reprodução no navegador.

## Observação
Esta é uma versão inicial front-end. O perfil e a lista de vídeos salvos ficam no `localStorage` do navegador. Ainda não possui cadastro real, banco de dados, upload de vídeos nem painel administrativo.


## Miniaturas e reprodução
As miniaturas ficam na pasta `img/` e são carregadas por elementos `<img>` nos cards. Troque o valor `thumbnail` de cada vídeo em `js/app.js` pelo caminho da sua imagem. O botão de play aparece sobre a miniatura; clicar no card abre o player. Para reproduzir um vídeo real, informe o caminho/URL MP4 na propriedade `url` do vídeo.


## Player e favoritos — V3
- Controles de play/pause, progresso, tempo, volume, mudo e tela cheia.
- Botão de coração para adicionar/remover vídeos dos favoritos.
- Nova página Favoritos no menu.
- Os favoritos ficam salvos no navegador via localStorage.
- Configure `url` em cada vídeo no `js/app.js` com o caminho/URL direto do MP4 para reprodução real.


## Miniatura EV Edits
A primeira miniatura usa `img/ev-edits-thumbnail.jpg`, criada a partir da arte enviada, ajustada para 16:9 sem cortar o cartaz. Para trocar, substitua esse arquivo ou altere o campo `thumbnail` do primeiro vídeo em `js/app.js`.


## V6 — Login, cadastro, planos e checkout demonstrativo
- Tela inicial com login por e-mail e senha e três planos: Mensal (30 dias/R$ 10,00), Bimestral (60 dias/R$ 60,00) e Semestral (180 dias/R$ 180,00).
- Cadastro com nome completo, e-mail, senha, país, cidade, bairro e número.
- Após cadastro e escolha do plano, abre a página de pagamento com QR do identificador informado.
- O QR foi gerado contendo literalmente `4bff2916-8ef2-4048-b0ef-5725143d5381`. Esse conteúdo não foi validado como payload PIX; não é garantia de que o QR permita pagamento.
- Login, cadastro e sessão são apenas demonstração usando localStorage. Senhas ficam no navegador sem proteção adequada. Não use dados reais/sensíveis nesta versão.
- Não há integração com banco de dados, autenticação segura, gateway PIX, confirmação automática nem liberação automática de assinatura. Para produção, implemente backend, hash de senhas, HTTPS e integração com provedor de pagamentos.
