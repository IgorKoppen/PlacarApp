# Projeto de Aplicativo de Placar

Este projeto é um aplicativo Android simples que permite acompanhar a pontuação de dois jogadores. O aplicativo fornece funcionalidade para aumentar a pontuação de cada jogador, reiniciar o placar e encerrar a partida.
<p align="center">
  <img src="https://github.com/IgorKoppen/PlacarApp/blob/main/screenshot/Screenshot_20241011_164205.png" alt="Captura de Tela do App" width="300"/>
</p>

## Funcionalidades

- **Incremento de Pontuação:** Aumente a pontuação de cada jogador pressionando os botões dedicados.
- **Reiniciar Partida:** Restaura o placar de ambos os jogadores para zero.
- **Salvar Estado:** O estado do jogo é salvo automaticamente em casos de interrupção (como mudanças de configuração do dispositivo).
- **Encerrar Partida:** Opção para finalizar o jogo e sair da tela de placar.

## Estrutura do Código

O aplicativo é composto pelo seguinte arquivo principal:

- `MainActivity.kt`: Contém a lógica principal da interface do usuário e manipulação de eventos.

### Componentes Chave

- **`ActivityMainBinding`**: Classe de binding gerada automaticamente para acessar as views do arquivo de layout XML sem o uso de `findViewById`.
- **`playerOneScore` e `playerTwoScore`**: Variáveis que armazenam a pontuação de cada jogador.
- **Métodos de Configuração**:
    - `setUpListeners()`: Configura os ouvintes de clique para os botões de interação no layout.
    - `setUpScorePlayerOne()` e `setUpScorePlayerTwo()`: Atualizam as text views com as pontuações atuais dos jogadores.
    - `restart()`: Reseta a pontuação dos jogadores para zero.

## Ciclo de Vida

O estado atual do jogo (pontuação de ambos os jogadores) é salvo no método `onSaveInstanceState()`. Quando a atividade é recriada (por exemplo, após uma rotação de tela), as pontuações são restauradas a partir do pacote `savedInstanceState`.

## Como Contribuir

1. Faça um fork deste repositório.
2. Crie sua feature branch: `git checkout -b minha-nova-funcionalidade`
3. Commit suas alterações: `git commit -m 'Adicionando nova funcionalidade'`
4. Envie para o branch: `git push origin minha-nova-funcionalidade`
5. Envie um Pull Request.

## Requisitos

- Android Studio instalado.
- Dispositivo ou emulador Android para testar o aplicativo.
