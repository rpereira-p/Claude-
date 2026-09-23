# Flappy Bird

Clone completo do Flappy Bird em HTML5 + JavaScript puro, sem dependências.
Funciona no navegador do computador e do celular, e pode ser instalado como
aplicativo (PWA) para jogar offline.

## Como jogar

- **Toque / clique / Espaço / ↑**: o pássaro bate as asas e sobe.
- Passe entre os canos para marcar pontos. Encostou em um cano ou no chão, fim de jogo.
- O recorde fica salvo no aparelho.
- Medalhas na tela de fim de jogo: bronze (10), prata (20), ouro (30), platina (40).

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

Toda a arte e os sons são originais, gerados em tempo de execução no canvas e
no WebAudio; nenhum recurso do jogo original é usado.
