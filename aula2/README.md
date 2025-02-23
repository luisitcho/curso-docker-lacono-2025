# Introdução

Este repositório é um aplicativo de exemplo para usuários que estão seguindo o guia de introdução em https://docs.docker.com/get-started/.

O aplicativo é baseado no tutorial de introdução disponível em https://github.com/docker/getting-started.

version: 1.0.1


<h2>Explicação dos Comandos Docker</h2>

<h2>1. Construção de Imagem</h2>
<p class="command">docker build -t app:v1.0.0 .</p>
<p>Cria uma imagem Docker com o nome <code>app</code> e a versão <code>v1.0.0</code>.</p>

<h2>2. Listar Imagens</h2>
<p class="command">docker images</p>
<p>Lista todas as imagens armazenadas localmente.</p>

<h2>3. Remover Imagem</h2>
<p class="command">docker image remove app:v1.0.0</p>
<p>Remove a imagem <code>app:v1.0.0</code> do sistema.</p>

<h2>4. Criar uma Nova Tag para uma Imagem</h2>
<p class="command">docker image tag 18ebc3d77198 luisitcho/app:v1</p>
<p>Cria uma nova referência (tag) para a imagem de ID <code>18ebc3d77198</code> como <code>luisitcho/app:v1</code>.</p>

<h2>5. Fazer Login no Docker Hub</h2>
<p class="command">docker login</p>
<p>Autentica o usuário no Docker Hub.</p>

<h2>6. Enviar uma Imagem para o Docker Hub</h2>
<p class="command">docker push luisitcho/app:v1</p>
<p>Faz o upload da imagem <code>luisitcho/app:v1</code> para o Docker Hub.</p>

<h2>7. Salvar uma Imagem como Arquivo</h2>
<p class="command">docker image save -o appv2.tar app:v2</p>
<p>Salva a imagem <code>app:v2</code> como um arquivo <code>appv2.tar</code> no sistema.</p>

<h2>8. Remover uma Imagem pelo ID</h2>
<p class="command">docker image rm -f 18ebc3d77198</p>
<p>Força a remoção da imagem com ID <code>18ebc3d77198</code>.</p>

<h2>9. Carregar uma Imagem a Partir de um Arquivo</h2>
<p class="command">docker image load -i appv2.tar</p>
<p>Carrega a imagem armazenada no arquivo <code>appv2.tar</code> de volta para o Docker.</p>