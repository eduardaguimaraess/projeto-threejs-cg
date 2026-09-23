# ISS 3D — Estação Espacial Internacional

Trabalho desenvolvido para a disciplina de Computação Gráfica, Realidade Virtual e Metaverso, implementado com a biblioteca Three.js.

## Integrantes

- Dyogo Antônio Silva Oliveira
- Eduarda Guimarães Monteiro
- Eduardo Vieira Torres dos Santos
- Gabriel Hawai Coelho Moreira da Silva
- Pedro Henrique De Oliveira Cadiz
- Thainara de Fátima Jacob Vieira

## Descrição do projeto

O projeto consiste na modelagem tridimensional da Estação Espacial Internacional (ISS), construída de forma modular a partir de seus principais segmentos: russo (Zvezda, Zarya, Nauka, Poisk, Rassvet), americano (Unity, Destiny, Tranquility, Quest, Leonardo, Cupola) e da proa (Harmony, Columbus, Kibo), além da treliça integrada, painéis solares, radiadores, antena de comunicações e o braço robótico Canadarm2.

A cena inclui ainda um satélite controlável pelo usuário e um ambiente de fundo composto por céu estrelado e representação decorativa da Terra.

A interação do usuário ocorre de três formas: controle da câmera por meio do mouse (rotação e zoom), movimentação do satélite através do teclado (WASD) e seleção dos módulos da estação por meio de clique, o que exibe informações referentes ao módulo selecionado (nome, agência responsável e descrição).

## Recursos utilizados

**Geometrias:** CylinderGeometry, SphereGeometry, ConeGeometry, BoxGeometry

**Materiais:** MeshStandardMaterial, aplicado à maior parte dos objetos, e MeshBasicMaterial, utilizado no céu estrelado e na chama do satélite, elementos que não requerem sombreamento

**Iluminação:** AmbientLight e DirectionalLight

**Texturas:** quatro texturas geradas proceduralmente por meio de canvas 2D (casco metálico, painel solar, radiador e céu estrelado), carregadas com TextureLoader e configuradas com repetição via repeat.set()

**Animações:**
- Rotação contínua da estação
- Oscilação periódica dos painéis solares (Math.sin)
- Movimentação do braço robótico Canadarm2 (Math.sin)
- Flutuação do satélite (Math.sin)

**Interação por teclado:** movimentação do satélite pelas teclas WASD e alternância de câmera entre a ISS e o satélite pela tecla C

**Interação por mouse:** utilização de Raycaster para seleção dos módulos da estação, com resposta visual e atualização de informações na interface

## Execução do projeto

Para executar o projeto, basta abrir o arquivo index.html em um navegador com suporte a WebGL e ES Modules. Não há necessidade de instalação de dependências, pois as bibliotecas são carregadas via CDN e as texturas são geradas em tempo de execução.
