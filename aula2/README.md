# Introdução

Este repositório é um aplicativo de exemplo para usuários que estão seguindo o guia de introdução do Docker disponível em:  
https://docs.docker.com/get-started/

O aplicativo é baseado no tutorial oficial disponível em:  
https://github.com/docker/getting-started

**Versão:** 1.0.1

---

## Explicação dos Comandos Docker

### 1. Construção de Imagem
```bash
docker build -t app:v1.0.0 .
```
Cria uma imagem Docker com o nome `app` e a versão `v1.0.0` a partir do **Dockerfile** no diretório atual (`.`).

---

### 2. Listar Imagens
```bash
docker images
```
Lista todas as imagens armazenadas localmente, mostrando nome, tag, ID, tamanho e data de criação.

---

### 3. Remover Imagem
```bash
docker image remove app:v1.0.0
```
Remove a imagem `app:v1.0.0` do sistema.  
Também pode ser usado o atalho:
```bash
docker rmi app:v1.0.0
```

---

### 4. Criar uma Nova Tag para uma Imagem
```bash
docker image tag 18ebc3d77198 luisitcho/app:v1
```
Cria uma nova referência (tag) para a imagem de ID `18ebc3d77198` com o nome `luisitcho/app:v1`.  
Isso é útil para renomear ou preparar a imagem para envio ao Docker Hub.

---

### 5. Fazer Login no Docker Hub
```bash
docker login
```
Autentica o usuário no Docker Hub, permitindo o envio (`push`) e o download (`pull`) de imagens privadas ou públicas.

---

### 6. Enviar uma Imagem para o Docker Hub
```bash
docker push luisitcho/app:v1
```
Envia a imagem `luisitcho/app:v1` para o repositório no Docker Hub.

---

### 7. Salvar uma Imagem como Arquivo
```bash
docker image save -o appv2.tar app:v2
```
Exporta a imagem `app:v2` para um arquivo chamado `appv2.tar`, que pode ser transferido ou armazenado como backup.

---

### 8. Remover uma Imagem pelo ID
```bash
docker image rm -f 18ebc3d77198
```
Força (`-f`) a remoção da imagem com ID `18ebc3d77198`, mesmo que esteja em uso por algum container parado.

---

### 9. Carregar uma Imagem a Partir de um Arquivo
```bash
docker image load -i appv2.tar
```
Importa uma imagem armazenada no arquivo `appv2.tar` de volta para o Docker.

---

> ⚠️ Nota:  Sempre verifique as imagens existentes antes de remover (`docker images`) para evitar apagar algo importante.
