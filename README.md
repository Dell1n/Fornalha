# Fornalha Industrial (Minecraft Bedrock)

Protótipo 3D de uma fornalha industrial modular para o Minecraft Bedrock, com simulação tick a tick.

- `index.html`: abra direto no navegador (precisa de internet para carregar o three.js e as fontes).
- `fornalha-industrial.html`: o mesmo conteúdo, sem o cabeçalho HTML (formato usado na publicação como Artifact).

## O que o protótipo mostra

- **2 arquiteturas**:
  - **Extrator 8×**: 2 baús, cada um sobre um carrinho-funil parado na quina de 4 funis; os 8 funis formam 4 correntes de 5 itens/s, uma para o carrinho distribuidor de cada módulo. Desligar um módulo é travar os 2 funis da quina dele.
  - **Carrinho por fileira**: o distribuidor da fileira é o próprio carrinho-funil parado embaixo do baú; módulos de 8 travados por linhas de redstone.
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
| Carrinho com funil puxando do baú | 1 item a cada 2 ticks (10 itens/s), segundo a Minecraft Wiki |
| Comparador | 1 + ⌊14 × ocupação⌋ |

Não confirmado para o Bedrock: se 4 funis conseguem puxar do mesmo carrinho-funil parado na quina (base do extrator 8×). A velocidade do carrinho-funil pode ser ajustada em “Parâmetros para calibrar no seu mundo”.
