# Jogo de Xadrez Console

![Xadrez](https://img.shields.io/badge/Chess-Console-blue)

Este repositório contém um jogo de xadrez jogável via console, desenvolvido em C#. O principal objetivo deste projeto é praticar e demonstrar conceitos de Programação Orientada a Objetos (aprendidos no curso da Udemy), aplicados no desenvolvimento de um jogo de tabuleiro.

## Conceitos de POO Aplicados

### 1. **Classes e Objetos**
   - **Circunstância:** Cada peça de xadrez (rei, rainha, torre, bispo, cavalo, peão) é representada por uma classe específica que herda de uma classe base `Peca`. O tabuleiro de xadrez é representado por uma classe `Tabuleiro`, que contém uma matriz de objetos `Peca`.
   - **Classes:** `Peca`, `Rei`, `Rainha`, `Torre`, `Bispo`, `Cavalo`, `Peao`, `Tabuleiro`.

### 2. **Herança**
   - **Circunstância:** As classes específicas das peças (ex: `Rei`, `Rainha`, etc.) herdam da classe base `Peca`, reutilizando e especializando funcionalidades comuns a todas as peças.
   - **Classes:** `Peca` (classe base), `Rei`, `Rainha`, `Torre`, `Bispo`, `Cavalo`, `Peao`.

### 3. **Polimorfismo**
   - **Circunstância:** O movimento de cada peça é determinado de acordo com a sua classe específica, utilizando métodos sobrecarregados na classe base `Peca`. Isso permite tratar diferentes tipos de peças de forma genérica durante o jogo.
   - **Métodos:** `Movimentar()`, `PodeMover()`.

### 4. **Encapsulamento**
   - **Circunstância:** Os atributos das classes estão encapsulados, sendo acessados e modificados apenas através de métodos específicos. Por exemplo, a posição das peças no tabuleiro é gerenciada pela classe `Tabuleiro` e não pode ser alterada diretamente por outras classes.
   - **Exemplo de Atributos Encapsulados:** `Posicao` da peça, `Pecas` do tabuleiro.

### 5. **Abstração**
   - **Circunstância:** A estrutura do jogo é modelada em alto nível, com classes que representam conceitos chave do xadrez (como `Tabuleiro`, `Peca`, `Jogador`). Detalhes específicos de implementação são escondidos do usuário final.
   - **Classes Abstratas e Interfaces:** `Peca`, `Movimento`.

## Funcionalidades

- **Movimentação de Peças:** Permite ao jogador mover as peças no tabuleiro de acordo com as regras do xadrez.
- **Verificação de Xeque:** Detecta se o rei está em xeque após um movimento.
- **Validação de Movimentos:** Apenas movimentos válidos são permitidos, de acordo com as regras do jogo.
- **Exibição do Tabuleiro:** O estado atual do tabuleiro é mostrado a cada turno.

## Jogadas Especiais

- **Roque:** Implementa o roque curto e o roque longo, permitindo ao rei e à torre moverem-se simultaneamente em uma jogada, desde que as condições necessárias sejam atendidas (nenhuma peça entre rei e torre, rei e torre não tenham se movido, rei não esteja em xeque).
- **Promoção de Peão:** Quando um peão atinge a última fileira do tabuleiro, ele pode ser promovido a uma rainha, torre, bispo ou cavalo, conforme a escolha do jogador.
- **En Passant:** Implementa a captura "en passant", onde um peão pode capturar outro peão que tenha avançado duas casas em seu movimento inicial, passando por uma casa que poderia ter sido capturada se tivesse avançado apenas uma casa.
- **Xeque-mate:** Verifica automaticamente se o movimento atual colocou o rei adversário em xeque-mate, encerrando o jogo se essa condição for atendida.

## Como Jogar

- Após iniciar o jogo, o tabuleiro será exibido no console.
- Digite os comandos seguindo as instruções para mover as peças.
- O jogo detectará automaticamente xeques, jogadas especiais e finalização do jogo.

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
