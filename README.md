# Entregas da Optativa - Experiências Imersivas

## Atividade Ponderada - Semana 1
Experiência que permita o usuário escolher entre rodar uma aplicação de realidade aumentada ou uma aplicação de realidade virtual (tour 360). <br>
Rspondenda as seguintes questões: <br><br>

- **O que foi desenvolvido?** <br>
Foi criada uma aplicação que permite ao usuário ter uma experiência de Realidade Virtual (VR), representada por um tour 360 interativo, com o ambiente do refeitório do Inteli e também o ambiente da lanchonete. No código fornecido, o foco está na implementação da parte de VR, utilizando A-Frame, um framework baseado em HTML para construção de experiências de realidade virtual na web. <br>

- **Como foi implementada a experiência de realidade aumentada?** <br>
Embora a experiência de AR ainda não esteja diretamente implementada no código, o projeto pode ser estendido para incluir AR utilizando tecnologias como o AR.js, que é compatível com A-Frame. O AR pode ser integrado adicionando marcadores como QR Codes/códigos de barra ou reconhecimento de imagens para interagir com objetos no mundo real. A ideia seria permitir ao usuário, ao abrir a aplicação, escolher AR e visualizar modelos 3D interagindo com seu ambiente físico, como por exemplo um ambiente de cozinha, utilizando um dispositivo móvel.

- **Como foi implementada a experiência de realidade virtual?**
  
A experiência de VR foi implementada através de:
  - A-Frame para criar um tour 360 interativo.
  - Câmera do celular e o aplicativo *360 Photo Cam*, com a fucnionalidade de tirar fotos no modo 360º para permitir interação do usuário com elementos virtuais, possibilitando rotacionar a imagem observando todo o ambiente e com a possibilidade de andar com (a,w,s,d) e também dar zoom.
  - Transições interativas, como o evento de clique na esfera vermelha para navegar para outra cena (simulada como segunda_tela.html), que no caso é o ambiente da cozinha do refeitório.
  - Assets que são pré-carregados para compor o ambiente imersivo. <br><br>

  O tour 360 é representado por um elemento \<a-sky>\, que carrega imagens esféricas para simular o ambiente. Objetos como a esfera vermelha \<a-sphere> adicionam interatividade, permitindo ao usuário "mover-se" para diferentes locais.

## Conclusão
Esta atividade ponderada foi desenvolvida para proporcionar uma experiência imersiva de Realidade Virtual (VR). A aplicação permite ao usuário explorar um tour 360 interativo em VR, em que os ambientes virtuais do Inteli são construídos com o framework A-Frame. A interação é implementada por meio de uma câmera e um aplicativo, que permite que o usuário exmplore o ambiente virtual, e que possui um botão que simula uma transição entre as duas cenas. Sendo assim, é possível entender que imagens esféricas são usadas para criar uma sensação de imersão, e elementos como texto e objetos interativos tornam a experiência mais dinâmica e informativa. No cenário atual, a atividade oferece uma demonstração funcional de VR. <br>

A parte de AR, ainda não foi implementada, está planejada para ser desenvolvida, para que os usuários interajam com objetos digitais do mundo real, utilizando seus dispositivos móveis. Com essa integração, será possível a escolha inicial entre VR e AR, criando uma aplicação mista para experiências digitais imersivas. Para executar a entrega atual, deve-se fazer um clone do repositório, abrir o servidor e executar a seguinte linha de código no terminal: node server.js. 

Link do site: 
