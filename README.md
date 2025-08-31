# Prótese Robótica de Mão

<p align="center">
  <img src="https://skillicons.dev/icons?i=androidstudio,dart,flutter" alt="Ícones de Dart & Flutter"/>
  <br/>
  <img src="https://skillicons.dev/icons?i=vscode,cpp" alt="Ícone de C++" />
</p>

Este é o resultado do projeto desenvolvido na Disciplina Projeto Integrado de Computação II.

O projeto consiste em uma integração completa de Hardware e Software desenvolvido pelo grupo para desenvolver uma prótese de mão funcional e com independência dos movimentos entre os dedos, com 3 graus de liberdade, executando a flexão/extensão nas três articulações (metacarpofalângica, interfalângica proximal, interfalângica distal).

Um ESP32 controla 5 servo motores que tensiona e relaxam um fio de pesca para realizar a flexão e, em conjunto com elásticos, realizar a extensão. Há também um sensor de pressão na palma da mão para detectar quando a mão segura algum objeto e controlar o movimento dos dedos.

A mão é controlada por um aplicativo de celular, onde é possível executar gestos pré definidos, criar seus próprios gestos e utilizar comandos de voz para controlar a mão.

<div align="center">

  | <img src="./assets/hand.jpeg" alt="Prótese" width="350px"/> | <video src="https://github.com/user-attachments/assets/fb7e4de5-c45f-4589-a4b7-9bfb23c6c3cd" controls></video> |
  |-----------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|

</div>

---

## 🌟 Motivação  

A limitação das funções da mão compromete a autonomia de milhões de pessoas.  

Nosso projeto busca desenvolver uma mão robótica acessível e funcional, unindo tecnologia, inclusão e aprendizado.  

Queremos tornar a robótica uma ferramenta real de transformação social.  

---

## 💡 A solução  

- **Uma mão robótica acessível e intuitiva, controlada pela voz.**  
- **Quebrando a Barreira do Custo** – Eliminamos a necessidade de sensores mioelétricos caros.  
- **Controle por Voz** – Comandos simples e diretos.  
- **Movimentos Realistas** – Design inspirado na anatomia humana.  
- **Plataforma Aberta** – A mesma tecnologia pode ser aplicada em robótica industrial, automação e muito mais.  

---

### 🎥 Vídeo do Pitch

Assista ao vídeo de apresentação do projeto no YouTube clicando na imagem abaixo:

<p align="center">
  <a href="https://youtu.be/Zz2Sscj2LH4" target="_blank">
    <img src="https://img.youtube.com/vi/Zz2Sscj2LH4/0.jpg" alt="Pitch da Prótese Robótica de Mão" width="70%"/>
  </a>
</p>

### 📄 Apresentação final:

Acesse a apresentação completa do projeto no link abaixo:

[📄 Mão Robótica.pdf](./documento/Mão%20Robótica.pdf)

---

## Módulos

O projeto é separado em 4 módulos:

-   [Software do App Mobile](#app)
-   [Estrutura da mão](#estrutura)
-   [Circuito eletrônico](#circuito)
-   [Software do controlador (ESP32)](#controlador)

### App

Desenvolvido com Dart e Flutter, o aplicativo se conecta ao ESP32 pelo Bluetooth e possibilita ao usuário enviar comandos de gestos pré definidos, criar seus próprios gestos, controlar dedos individualmente e executar os gestos salvos a partir de comandos de voz.

Veja com mais detalhes em: [Aplicativo](https://github.com/jcquadros/app_protese_robotica_de_mao)

<div align="center">
  <img src="./assets/screenshot_1.png" alt="Tela de Gestos Salvos" width="30%"/>
  <img src="./assets/screenshot_2.png" alt="Tela de Gestos Personalizáveis" width="30%"/>
  <img src="./assets/screenshot_3.png" alt="Tela de Comando de voz" width="30%"/>
</div>

### Estrutura

A estrutura foi desenvolvida com Impressão 3D e modificações artesanais. Foi utilizado o modelo disponível em [InMoov](https://inmoov.fr/).

Servos Motores são utilizados para tensionar uma linha de pesca que realiza a flexão dos dedos e um elástico mantém os dedos tensionados para realizar a extensão.

Veja com mais detalhes em: [Estrutura](./Estrutura/)

### Circuito

Foi confeccionada uma placa de circuito para conectar o ESP32 aos motores, fontes e ao sensor de pressão. Garantindo melhor estrutura e menos ruídos e falhas, em comparação com um circuito em Protoboard.

Veja com mais detalhes em: [Circuito](./Circuito/)

<div align="center">
    <img src="./Circuito/assets/schematics.png" width="80%" alt="Diagrama do Circuito"/>
</div>

### Controlador

Este é o Sistema do ESP32. Desenvolvido com C++ através da plataforma Arduino IDE.

Através de um JSON recebido pelo aplicativo mobile através do Bluetooth, a mão converte os valores (que vem em % de flexão dos dedos) para ângulos, onde cada dedo tem seus ângulos mínimo e máximo.

E assim, enviando os ângulos para os dedos correspondentes, verificando a pressão no sensor da palma para confirmar que não há objetos na mão bloqueando a flexão dos dedos.

Veja com mais detalhes em: [Controlador ESP32](https://github.com/jcquadros/controlador-protese-robotica-de-mao)

---

## Equipe

| [<img src="https://avatars.githubusercontent.com/u/84464307?s=400&u=e9879bb9f28ab7ca900513a3323bcf3fcbfcd68e&v=4" width=110 alt="David Propato"><br><sub>David Propato</sub>](https://github.com/Propato) | [<img src="https://avatars.githubusercontent.com/u/72812365?v=4" width=110 alt="Gustavo Sarti"><br><sub>Gustavo Sarti</sub>](https://github.com/gustavosarti) | [<img src="https://avatars.githubusercontent.com/u/109080878?v=4" width=110 alt="Jullie Quadros"><br><sub>Jullie Quadros</sub>](https://github.com/jcquadros) | [<img src="https://avatars.githubusercontent.com/u/69646100?v=4" width=110 alt="Mateus Sartorio"><br><sub>Mateus Sartorio</sub>](https://github.com/mateus-sartorio) |
| :-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------: | -------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------------------------------------------------------------------------- |

---

## 📌 Conclusão  

Este projeto vai além de um protótipo acadêmico: ele mostra como a união de **hardware acessível, software inteligente e design inspirado na anatomia humana** pode gerar soluções reais e de impacto social.  

A **Prótese Robótica de Mão** entrega movimentos independentes, controle intuitivo por aplicativo e comandos de voz, além de um custo reduzido ao eliminar tecnologias caras como sensores mioelétricos. Isso torna a solução **mais próxima das pessoas que realmente precisam dela**.  

Além do impacto social, o projeto também serve como **plataforma aberta e extensível**, capaz de ser aplicada em outros cenários, como **robótica industrial, automação e pesquisa acadêmica**.  

Com isso, buscamos mostrar que a robótica não é apenas uma área de alta tecnologia, mas também uma **ferramenta de inclusão, acessibilidade e transformação social**, aproximando inovação de quem mais precisa dela.  

---
