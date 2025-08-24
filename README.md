# Prótese Robótica de Mão

<p align="center">
  <img src="https://skillicons.dev/icons?i=dart,flutter,cpp" /> <br/>
</p>

Este é o resultado do projeto desenvolvido na Disciplina Projeto Integrado de Computação II.

O projeto consiste em uma integração completa de Hardware e Software desenvolvido pelo grupo para desenvolver uma prótese de mão funcional e com independência dos movimentos entre os dedos, com 3 graus de liberdade, executando a flexão/extensão nas três articulações (metacarpofalângica, interfalângica proximal, interfalângica distal).

Um ESP32 controla 5 servo motores que tensiona e relaxam um fio de pesca para realizar a flexão e, em conjunto com elásticos, realizar a extensão. Há também um sensor de pressão na palma da mão para detectar quando a mão segura algum objeto e controlar o movimento dos dedos.

A mão é controlada por um aplicativo de celular, onde é possível executar gestos pré definidos, criar seus próprios gestos e utilizar comandos de voz para controlar a mão.

<div align="center">
  <img src="https://github.com/mateus-sartorio/ecommerce-app/blob/main/assets/images/pic1.png" alt="" width="30%"/>
  <img src="https://github.com/mateus-sartorio/ecommerce-app/blob/main/assets/images/pic2.png" alt="" width="30%"/>
</div>

## Módulos

O projeto é separado em 4 módulos:

-   [Estrutura da mão](###Estrutura)
-   [Circuito eletrônico](###Circuito)
-   [Software do controlador (ESP32)](###Controlador)
-   [Software do App Mobile](###App)

### Estrutura

A estrutura foi desenvolvida com Impressão 3D e modificações artesanais. Foi utilizado o modelo disponível em [InMoov](https://inmoov.fr/).

Servos Motores são utilizados para tensionar uma linha de pesca que realiza a flexão dos dedos e um elástico mantém os dedos tensionados para realizar a extensão.

Veja com mais detalhes em: [Estrutura](./Estrutura/)

### Circuito

Foi confeccionada uma placa de circuito para conectar o ESP32 aos motores, fontes e ao sensor de pressão. Garantindo melhor estrutura e menos ruídos e falhas, em comparação com um circuito em Protoboard.

Veja com mais detalhes em: [Circuito](./Circuito/)

### Controlador

Este é o Sistema do ESP32. Desenvolvido com C++ através da plataforma Arduino IDE.

Através de um JSON recebido pelo aplicativo mobile através do Bluetooth, a mão converte os valores (que vem em % de flexão dos dedos) para ângulos, onde cada dedo tem seus ângulos mínimo e máximo.

E assim, enviando os ângulos para os dedos correspondentes, verificando a pressão no sensor da palma para confirmar que não há objetos na mão bloqueando a flexão dos dedos.

Veja com mais detalhes em: [Controlador ESP32](github.com/)

### App

Desenvolvido com Dart e Flutter, o aplicativo se conecta ao ESP32 pelo Bluetooth e possibilita ao usuário enviar comandos de gestos pré definidos, criar seus próprios gestos, controlar dedos individualmente e executar os gestos salvos a partir de comandos de voz.

Veja com mais detalhes em: [Aplicativo](github.com/)

## Equipe

| [<img src="https://avatars.githubusercontent.com/u/84464307?s=400&u=e9879bb9f28ab7ca900513a3323bcf3fcbfcd68e&v=4" width=110 alt="David Propato"><br><sub>David Propato</sub>](https://github.com/Propato) | [<img src="" width=110 alt="Gustavo Sarti"><br><sub>Gustavo Sarti</sub>](https://github.com) | [<img src="https://avatars.githubusercontent.com/u/109080878?v=4" width=110 alt="Jullie Quadros"><br><sub>Jullie Quadros</sub>](https://github.com/jcquadros) | [<img src="https://avatars.githubusercontent.com/u/69646100?v=4" width=110 alt="Mateus Sartorio"><br><sub>Mateus Sartorio</sub>](https://github.com/mateus-sartorio) |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
