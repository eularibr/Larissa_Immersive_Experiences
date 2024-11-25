# Entregas da Optativa - Experiências Imersivas

## Atividade Ponderada - Semana 1
Experiência que permita o usuário escolher entre rodar uma aplicação de realidade aumentada ou uma aplicação de realidade virtual (tour 360). <br>

## **1. O que foi desenvolvido?** <br>

**Entrega Tour 360:** <br>

Foi criada uma aplicação que permite ao usuário ter uma experiência de Realidade Virtual (VR), representada por um tour 360 interativo, com o ambiente do refeitório do Inteli e também o ambiente da lanchonete. No código fornecido, o foco está na implementação da parte de VR, utilizando A-Frame, um framework baseado em HTML para construção de experiências de realidade virtual na web. <br>

**Entrega AR (Imagem):** <br>

Foi criada uma aplicação de Realidade Aumentada (AR) utilizando o framework A-Frame com suporte ao AR.js. O projeto demonstra um modelo 3D de um objeto (no caso, "shiba"), que aparece quando o usuário aponta a câmera de um dispositivo para um marcador AR específico, chamado de "hiro". Adicionalmente, a interface inclui um botão de retorno fixo, permitindo que o usuário volte para a tela inicial da aplicação, garantindo uma navegação fluida.


**Entrega AR (Vídeo _Som):** <br>

Foi criada uma aplicação de Realidade Aumentada (AR) com integração de vídeos e áudio. O projeto utiliza o A-Frame e o AR.js para exibir um vídeo (#kuka) em um marcador específico (hiro), além de reproduzir um áudio associado. A funcionalidade inclui um componente chamado controlador, que pausa ou reproduz o vídeo e o áudio automaticamente com base na visibilidade do marcador "hiro". Um botão de retorno escrito "Volta" também foi adicionado para facilitar a navegação até a tela inicial da atividade.

## **2. Como foi implementada a experiência de realidade aumentada?** <br>

**Entrega Tour 360:** <br>

Embora a experiência de AR ainda não esteja diretamente implementada no código, o projeto pode ser estendido para incluir AR utilizando tecnologias como o AR.js, que é compatível com A-Frame. O AR pode ser integrado adicionando marcadores como QR Codes/códigos de barra ou reconhecimento de imagens para interagir com objetos no mundo real. A ideia seria permitir ao usuário, ao abrir a aplicação, escolher AR e visualizar modelos 3D interagindo com seu ambiente físico, como por exemplo um ambiente de cozinha, utilizando um dispositivo móvel.

**Entrega AR (Imagem):** <br>

A experiência de AR foi implementada com o AR.js em conjunto com o A-Frame, a funcionalidade depende do uso de um marcador físico chamado "hiro", que serve como ponto de referência para apresentar o modelo 3D. Desse modo, o modelo é carregado por meio de um \<a-assets>\ que define o recurso 3D, e o componente \<a-marker>\ vincula o modelo ao marcador. Logo, quando a câmera detecta o marcador, o modelo "shiba" é mostrado no espaço virtual, sobreposto ao mundo real. 

**Entrega AR (Vídeo _Som):** <br>

A experiência de AR foi implementada usando o A-Frame e o AR.js. Um marcador hiro foi configurado com um componente personalizado (controlador) para gerenciar a reprodução de um vídeo (#kuka) e um áudio (#som). Quando o marcador é detectado pela câmera, o vídeo e o áudio são reproduzidos automaticamente, e quando o marcador sai de vista, ambos são pausados. A lógica de controle foi desenvolvida no componente controlador utilizando os ciclos de inicialização (init) e atualização contínua (tick) do A-Frame, que monitoram a visibilidade do marcador.


## **3. Como foi implementada a experiência de realidade virtual?**
  
A experiência de VR foi implementada através de:
  - A-Frame para criar um tour 360 interativo.
  - Câmera do celular e o aplicativo *360 Photo Cam*, com a fucnionalidade de tirar fotos no modo 360º para permitir interação do usuário com elementos virtuais, possibilitando rotacionar a imagem observando todo o ambiente e com a possibilidade de andar com (a,w,s,d) e também dar zoom.
  - Transições interativas, como o evento de clique na esfera vermelha para navegar para outra cena (simulada como segunda_tela.html), que no caso é o ambiente da cozinha do refeitório.
  - Assets que são pré-carregados para compor o ambiente imersivo. <br><br>

  O tour 360 é representado por um elemento \<a-sky>, que carrega imagens esféricas para simular o ambiente. Objetos como a esfera vermelha \<a-sphere> adicionam interatividade, permitindo ao usuário "mover-se" para diferentes locais.

**Entrega AR (Imagem):** <br>

Nesta implementação, a experiência de Realidade Virtual (VR) não foi desenvolvida diretamente. O código é exclusivamente voltado para AR, uma vez que o atributo vr-mode-ui="enabled: false" desativa a interface de VR no A-Frame. Para integrar VR, seria necessário adicionar elementos como \<a-sky> ou \<a-camera> configurados para criar ambientes 360°, ou cenas interativas projetadas para visualização em dispositivos de VR.

**Entrega AR (Vídeo _Som):** <br>

Nesta implementação, não há uma experiência direta de Realidade Virtual (VR). O atributo vr-mode-ui="enabled: false" desativa a interface de VR no A-Frame, indicando que o projeto é focado em AR, logo, para adicionar VR, seria necessário configurar um ambiente imersivo com elementos como \<a-sky> ou utilizar outros componentes de VR no A-Frame, permitindo uma navegação em uma cena virtual sem a necessidade de marcadores físicos.

## Conclusão

Esta atividade foi elaborada para oferecer experiências imersivas tanto em Realidade Virtual (VR) quanto em Realidade Aumentada (AR), utilizando o framework A-Frame e a extensão AR.js. No contexto de VR, foi implementado um tour 360 interativo que permite-se explorar oa ambientes virtuais do Inteli, como a lanchonete e o refeitório. As imagens esféricas que foram utilizadas para criar uma sensação de imersão, enquanto os textos informativos e objetos clicáveis, tornam a navegação mais fluída. A transição entre cenas foi implementada simulando mudanças de ambiente, e o uso de um botão de navegação facilita a experiência. A aplicação demonstra de forma funcional como VR pode ser usado para explorar espaços virtuais de maneira inovadora e interativa.

Quanto à AR, foram criados dois cenários com funcionalidades distintas, em um deles, um modelo 3D é exibido sobre um marcador físico, enquanto no outro, um vídeo e áudio são reproduzidos automaticamente com base na detecção do marcador "hiro". A lógica de controle utilizada no código garante que o conteúdo pause ou retome conforme a visibilidade do marcador, enriquecendo a interação com o ambiente físico e digital. 

Para executar o projeto atual, basta clonar o repositório, iniciar o servidor e executar node server.js no terminal.
