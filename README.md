# Fornalha Industrial (Minecraft Bedrock)

Protótipo 3D de uma fornalha industrial modular para o Minecraft Bedrock, com simulação tick a tick.

- `index.html`: abra direto no navegador (precisa de internet para carregar o three.js e as fontes).
- `fornalha-industrial.html`: o mesmo conteúdo, sem o cabeçalho HTML (formato usado na publicação como Artifact).

## O que o protótipo mostra

- **3 formatos**: baú em cima, caixa de sapato (baús na lateral) e subterrâneo.
- **Módulos de 8 fornalhas** (1 a 4 por carrinho, 1 ou 2 fileiras), com 1 ou 2 vias de carga por carrinho.
- **Distribuição por carrinho-funil vai-e-vem**: cada funil destravado puxa 1 item por passada.
- **Combustível** por um segundo carrinho-funil no trilho de trás, só para as fornalhas ligadas.
- **Seleção automática**: o comparador lê o carrinho no trilho detector (força 3/6/9/12 para 1–4 packs) e trava os funis dos módulos que não precisam ligar.
- **Análise**: tempo para queimar 1 pack e vazão com fila grande em função do número de fornalhas e de vias, consumo de carvão, lista de materiais.

## Números do jogo usados

| Item | Valor |
|---|---|
| Fornalha | 200 ticks (10 s) por item |
| Alto-forno / defumador | 100 ticks (5 s) por item |
| Carvão | 8 itens |
| Funil | 1 item a cada 8 ticks (2,5 itens/s) |
| Carrinho | ~8 blocos/s (ajustável) |
| Comparador | 1 + ⌊14 × ocupação⌋ |

A velocidade com que o carrinho-funil puxa do baú pode variar entre versões; ajuste em “Parâmetros para calibrar no seu mundo”.
