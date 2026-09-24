# Flappy Bird

Clone completo do Flappy Bird em HTML5 + JavaScript puro, sem dependências.
Funciona no navegador do computador e do celular, e pode ser instalado como
aplicativo (PWA) para jogar offline.

## Jogar online

O jogo é publicado automaticamente no GitHub Pages a cada push:
**https://rpereira-p.github.io/Claude-/**

No celular, abra o link e use "Adicionar à tela inicial" para instalar como app.

## Como jogar

- **Toque / clique / Espaço / ↑**: o pássaro bate as asas e sobe.
- Passe entre os canos para marcar pontos. Encostou em um cano ou no chão, fim de jogo.
- O recorde fica salvo no aparelho.
- Medalhas na tela de fim de jogo: bronze (10), prata (20), ouro (30), platina (40).
- A partir de 50 pontos a velocidade sobe até travar nos 100.
- **Moedas** aparecem em alguns canos (10 a cada 30) e compram pássaros e cenários na **Loja**.
- **Power-ups** raros nos canos: escudo (aguenta uma batida), ímã (puxa moedas) e câmera lenta.
- **Ranking** por pássaro e por cenário com estrelas (10/25/50/100/200 pontos).
- **Desafios**: metas cumulativas por pássaro/cenário, desafios gerais e 3 desafios diários.
- Botões de som e música na tela inicial; pausa pelo botão, tecla P ou ao sair do app.

## Rodando

Abra o `index.html` direto no navegador, ou sirva a pasta com qualquer servidor
estático (necessário para instalar como app e para o modo offline):

```bash
python3 -m http.server 8000
# depois acesse http://localhost:8000
```

No celular, abra a página e use "Adicionar à tela inicial" para instalar.

## Estrutura

| Arquivo         | Conteúdo                                                     |
| --------------- | ------------------------------------------------------------ |
| `index.html`    | Jogo inteiro: sprites em pixel art gerados por código, física, telas e sons sintetizados |
| `manifest.json` | Metadados do PWA (nome, ícones, tela cheia em retrato)        |
| `sw.js`         | Service worker que faz cache dos arquivos para uso offline    |
| `icon-*.png`    | Ícones do app                                                |
| `.github/workflows/pages.yml` | Publica no GitHub Pages a cada push            |

Toda a arte e os sons são originais, gerados em tempo de execução no canvas e
no WebAudio; nenhum recurso do jogo original é usado.
