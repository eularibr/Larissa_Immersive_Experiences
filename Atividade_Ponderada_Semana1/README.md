# Entregas da Optativa - Experiências Imersivas

# Atividade Ponderada - Semana 1

Link do site: https://eularibr.github.io/Larissa_Immersive_Experiences/

Experiência que permita o usuário escolher entre rodar uma aplicação de realidade aumentada ou uma aplicação de realidade virtual (tour 360). <br>

## **1. O que foi desenvolvido?** <br>

### Entrega Tour 360: <br>

Foi criada uma aplicação que permite ao usuário ter uma experiência de Realidade Virtual (VR), representada por um tour 360 interativo, com o ambiente do refeitório do Inteli e também o ambiente da lanchonete. No código fornecido, o foco está na implementação da parte de VR, utilizando A-Frame, um framework baseado em HTML para construção de experiências de realidade virtual na web. <br>

<div align="center">
    <img src="https://github.com/eularibr/Larissa_Immersive_Experiences/blob/main/Demonstracoes_Imagens/Demonstracao_360_Lanchonete_Modulo12.png" 
         style="width: 70%; height: auto;"/> <br>
</div>

<div align="center">
  <img src="https://github.com/eularibr/Larissa_Immersive_Experiences/blob/main/Demonstracoes_Imagens/Demonstracao_360_Refeitorio_Modulo12.png"
        style="width: 70%; height: auto;"/> <br>
</div>

### Primeiro Arquivo (`index.html`)

#### Assets Carregados:
- Carrega duas imagens:
  - `cozinha_refeitorio_inteli.jpg`.
  - `lanchonete_inteli.jpg`.

#### Cenário 360°:
- Configura o céu (`a-sky`) para exibir a imagem **lanchonete_inteli.jpg**.
- Insere textos descritivos:
  - **"Lanchonete Inteli"** (título).
  - **"Local de lanche"** (descrição adicional).

#### Elemento Interativo:
- Adiciona uma esfera vermelha como botão (`#vai_para_cima`).
- Localiza a esfera em `(x = -8, y = 10, z = -26)`.

#### Transição de Tela:
- Um script detecta quando o cursor "entra" na esfera e redireciona para `segunda_tela.html`.

---

### Segundo Arquivo (`segunda_tela.html`)

#### Assets Carregados:
- Mesmos recursos do primeiro arquivo:
  - Carrega `cozinha_refeitorio_inteli.jpg` e `lanchonete_inteli.jpg`.

#### Cenário 360°:
- Configura o céu (`a-sky`) para exibir a imagem **cozinha_refeitorio_inteli.jpg**.
- Insere textos descritivos:
  - **"Refeitório do Inteli"** (título).
  - **"Local de preparo refeições"** (descrição adicional).

#### Elemento Interativo:
- Adiciona uma esfera vermelha como botão (`#vai_para_cima`).
- Localiza a esfera em `(x = -8, y = 10, z = -26)`.

#### Transição de Tela:
- Um script redireciona para `index.html` quando o cursor interage com a esfera.


### Como Funciona:
1. O **arquivo `index.html`** exibe o ambiente da **lanchonete**.
2. Ao interagir com a esfera, o usuário é redirecionado para o **arquivo `segunda_tela.html`**.
3. O **arquivo `segunda_tela.html`** exibe o ambiente do **refeitório**.
4. A navegação entre os ambientes é feita através do cursor 3D que detecta interação com os botões esféricos.

---

### Entrega AR (Imagem): <br>

Foi criada uma aplicação de Realidade Aumentada (AR) utilizando o framework A-Frame com suporte ao AR.js. O projeto demonstra um modelo 3D de um objeto (no caso, "shiba"), que aparece quando o usuário aponta a câmera de um dispositivo para um marcador AR específico, chamado de "hiro". Adicionalmente, a interface inclui um botão de retorno fixo, permitindo que o usuário volte para a tela inicial da aplicação, garantindo uma navegação fluida.

<div align="center">
  <img src="https://github.com/eularibr/Larissa_Immersive_Experiences/blob/main/Demonstracoes_Imagens/Demonstracao_AR_Shiba_Modulo12.png"
        style="width: 70%; height: auto;"/> <br>
</div>

### Funcionalidades

#### Cenário A-Frame
- Define um cenário (`<a-scene>`) com:
  - **Modo VR desativado**: `vr-mode-ui="enabled: false"`.
  - **UI de debug desativada para AR**: `debugUIEnabled:false`.

#### Recursos 3D
- Carrega um modelo 3D (`scene.gltf`) e o associa ao identificador `shiba`.

#### Marcador AR
- Associa um marcador AR do tipo **"hiro"** para exibir o modelo 3D quando o marcador é detectado.
- Renderiza o modelo `#shiba` sobre o marcador.

#### Câmera
- Configura uma câmera para capturar a experiência de AR no cenário.

#### Botão de Voltar
- Cria um botão fixo no canto superior esquerdo.
- Ao clicar no botão, redireciona o usuário para outra página chamada **"tela_inicial.html"**.

---

### Entrega AR (Vídeo _Som): <br>

Foi criada uma aplicação de Realidade Aumentada (AR) com integração de vídeos e áudio. O projeto utiliza o A-Frame e o AR.js para exibir um vídeo (#kuka) em um marcador específico (hiro), além de reproduzir um áudio associado. A funcionalidade inclui um componente chamado controlador, que pausa ou reproduz o vídeo e o áudio automaticamente com base na visibilidade do marcador "hiro". Um botão de retorno escrito "Volta" também foi adicionado para facilitar a navegação até a tela inicial da atividade.

<div align="center">
  <img src="https://github.com/eularibr/Larissa_Immersive_Experiences/blob/main/Demonstracoes_Imagens/Demonstracao_AR_video_e_som_Modulo12.png"
        style="width: 70%; height: auto;"/> <br>
</div>

<br>

### Funcionalidades

#### Cenário A-Frame
- Define um cenário (`<a-scene>`) com:
  - **Modo VR desativado**: `vr-mode-ui="enabled: false`.
  - **UI de debug desativada**: `debugUIEnabled:false`.

#### Recursos
- Carrega os seguintes recursos:
  - Um arquivo de áudio (`musica01.mp3`) com o ID `som`.
  - Um vídeo (`robos.mp4`) com o ID `kuka`, configurado para reprodução automática em loop.
  - Uma imagem (`025.png`) com o ID `sete`.

#### Marcador AR
- Associa um marcador AR tipo **"hiro"** para exibir:
  - Um vídeo (`#kuka`) ajustado em uma tela de largura e altura 1, rotacionada e posicionada sobre o marcador.

#### Câmera
- Configura uma câmera para capturar a experiência de AR.

#### Botão de Voltar
- Cria um botão fixo no canto superior esquerdo.
- Ao clicar, redireciona o usuário para outra página chamada **"tela_inicial.html"**.

#### Componente Controlador
- Registra um componente personalizado chamado `controlador` que:
  - **Monitora a visibilidade do marcador**:
    - Pausa o áudio (`#som`) e o vídeo (`#kuka`) quando o marcador não está visível.
    - Reproduz o áudio e o vídeo quando o marcador está visível.
  - Garante a **sincronização automática** entre áudio e vídeo.

#### Resultado
- Exibe um vídeo e toca uma música ao detectar o marcador **"hiro"**.
- Pausa o áudio e o vídeo automaticamente quando o marcador deixa de ser visível.

<br>

## **2. Como foi implementada a experiência de realidade aumentada?** <br>

### Entrega Tour 360: <br>

Embora a experiência de AR ainda não esteja diretamente implementada no código, o projeto pode ser estendido para incluir AR utilizando tecnologias como o AR.js, que é compatível com A-Frame. O AR pode ser integrado adicionando marcadores como QR Codes/códigos de barra ou reconhecimento de imagens para interagir com objetos no mundo real. A ideia seria permitir ao usuário, ao abrir a aplicação, escolher AR e visualizar modelos 3D interagindo com seu ambiente físico, como por exemplo um ambiente de cozinha, utilizando um dispositivo móvel.

### Entrega AR (Imagem): <br>

A experiência de AR foi implementada com o AR.js em conjunto com o A-Frame, a funcionalidade depende do uso de um marcador físico chamado "hiro", que serve como ponto de referência para apresentar o modelo 3D. Desse modo, o modelo é carregado por meio de um \<a-assets>\ que define o recurso 3D, e o componente \<a-marker>\ vincula o modelo ao marcador. Logo, quando a câmera detecta o marcador, o modelo "shiba" é mostrado no espaço virtual, sobreposto ao mundo real. 

### Entrega AR (Vídeo _Som): <br>

A experiência de AR foi implementada usando o A-Frame e o AR.js. Um marcador hiro foi configurado com um componente personalizado (controlador) para gerenciar a reprodução de um vídeo (#kuka) e um áudio (#som). Quando o marcador é detectado pela câmera, o vídeo e o áudio são reproduzidos automaticamente, e quando o marcador sai de vista, ambos são pausados. A lógica de controle foi desenvolvida no componente controlador utilizando os ciclos de inicialização (init) e atualização contínua (tick) do A-Frame, que monitoram a visibilidade do marcador.

<br>

## **3. Como foi implementada a experiência de realidade virtual?**

### Entrega Tour 360: <br>
  
A experiência de VR foi implementada através de:
  - A-Frame para criar um tour 360 interativo.
  - Câmera do celular e o aplicativo *360 Photo Cam*, com a fucnionalidade de tirar fotos no modo 360º para permitir interação do usuário com elementos virtuais, possibilitando rotacionar a imagem observando todo o ambiente e com a possibilidade de andar com (a,w,s,d) e também dar zoom.
  - Transições interativas, como o evento de clique na esfera vermelha para navegar para outra cena (simulada como segunda_tela.html), que no caso é o ambiente da cozinha do refeitório.
  - Assets que são pré-carregados para compor o ambiente imersivo. <br><br>

  O tour 360 é representado por um elemento \<a-sky>, que carrega imagens esféricas para simular o ambiente. Objetos como a esfera vermelha \<a-sphere> adicionam interatividade, permitindo ao usuário "mover-se" para diferentes locais.

### Entrega AR (Imagem): <br>

Nesta implementação, a experiência de Realidade Virtual (VR) não foi desenvolvida diretamente. O código é exclusivamente voltado para AR, uma vez que o atributo vr-mode-ui="enabled: false" desativa a interface de VR no A-Frame. Para integrar VR, seria necessário adicionar elementos como \<a-sky> ou \<a-camera> configurados para criar ambientes 360°, ou cenas interativas projetadas para visualização em dispositivos de VR.

### Entrega AR (Vídeo _Som): <br>

Nesta implementação, não há uma experiência direta de Realidade Virtual (VR). O atributo vr-mode-ui="enabled: false" desativa a interface de VR no A-Frame, indicando que o projeto é focado em AR, logo, para adicionar VR, seria necessário configurar um ambiente imersivo com elementos como \<a-sky> ou utilizar outros componentes de VR no A-Frame, permitindo uma navegação em uma cena virtual sem a necessidade de marcadores físicos.

<br>

## Conclusão

Esta atividade foi elaborada para oferecer experiências imersivas tanto em Realidade Virtual (VR) quanto em Realidade Aumentada (AR), utilizando o framework A-Frame e a extensão AR.js. No contexto de VR, foi implementado um tour 360 interativo que permite-se explorar oa ambientes virtuais do Inteli, como a lanchonete e o refeitório. As imagens esféricas que foram utilizadas para criar uma sensação de imersão, enquanto os textos informativos e objetos clicáveis, tornam a navegação mais fluída. A transição entre cenas foi implementada simulando mudanças de ambiente, e o uso de um botão de navegação facilita a experiência. A aplicação demonstra de forma funcional como VR pode ser usado para explorar espaços virtuais de maneira inovadora e interativa.

Quanto à AR, foram criados dois cenários com funcionalidades distintas, em um deles, um modelo 3D é exibido sobre um marcador físico, enquanto no outro, um vídeo e áudio são reproduzidos automaticamente com base na detecção do marcador "hiro". A lógica de controle utilizada no código garante que o conteúdo pause ou retome conforme a visibilidade do marcador, enriquecendo a interação com o ambiente físico e digital. 

Para executar o projeto atual, basta clonar o repositório, iniciar o servidor e executar node server.js no terminal.

<br><br>
