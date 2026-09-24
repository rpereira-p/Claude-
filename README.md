# Skyhop

Jogo de voo em pixel art para navegador e celular, em HTML5 + JavaScript puro,
sem dependências. Toque para bater as asas, passe entre os obstáculos, colete
moedas e desbloqueie pássaros e cenários. Pode ser instalado como aplicativo
(PWA) e funciona offline.

## Jogar online

Publicado automaticamente no GitHub Pages a cada push:
**https://rpereira-p.github.io/Claude-/**

No celular, abra o link e use "Adicionar à tela inicial" para instalar como app.

## Como jogar

- **Toque / clique / Espaço / ↑**: o pássaro bate as asas e sobe.
- Passe entre os obstáculos para marcar pontos. Encostou em um deles ou no chão, fim de jogo.
- A partir de 50 pontos a velocidade sobe até travar nos 100.
- Medalhas na tela de fim de jogo: bronze (10), prata (20), ouro (30), platina (40).
- **Moedas** aparecem em alguns vãos (10 a cada 30) e compram pássaros e cenários na **Loja**.
- **Power-ups** raros: escudo (aguenta uma batida), ímã (puxa moedas) e câmera lenta.
- **Ranking** por pássaro e por cenário com estrelas (10/25/50/100/200 pontos).
- **Desafios**: metas cumulativas por pássaro/cenário, desafios gerais e 3 desafios diários.
- Botões de som e música na tela inicial; pausa pelo botão, tecla P ou ao sair do app.
- Todo o progresso (recordes, moedas, compras, desafios) fica salvo no aparelho.

## Conteúdo

- **13 pássaros** em quatro raridades, incluindo o Em Chamas (fogo simulado por partículas) e o Arco-íris.
- **9 cenários** com efeitos próprios: Dia, Noite, Pôr do sol, Deserto, Neve, Guerra, Espaço, Vulcão e Neon.

## Rodando localmente

Abra o `index.html` direto no navegador, ou sirva a pasta com qualquer servidor
estático (necessário para instalar como app e para o modo offline):

```bash
python3 -m http.server 8000
# depois acesse http://localhost:8000
```

## Estrutura

| Arquivo         | Conteúdo                                                     |
| --------------- | ------------------------------------------------------------ |
| `index.html`    | Jogo inteiro: sprites em pixel art gerados por código, física, telas, música e sons sintetizados |
| `manifest.json` | Metadados do PWA (nome, ícones, tela cheia em retrato)        |
| `sw.js`         | Service worker: rede primeiro, cache como reserva para uso offline |
| `icon-*.png`    | Ícones do app                                                |
| `.github/workflows/pages.yml` | Publica no GitHub Pages a cada push            |

Toda a arte, a música e os sons são originais, gerados em tempo de execução no
canvas e no WebAudio. A fonte de pixel é a
[Press Start 2P](https://fonts.google.com/specimen/Press+Start+2P) (licença OFL),
carregada do Google Fonts.
