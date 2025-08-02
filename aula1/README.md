# Comandos Docker para este projeto

Cria a imagem com base nas configurações do `Dockerfile`:
```
docker build -t hi-docker .
```
> Cria uma imagem chamada `hi-docker` a partir do `Dockerfile` na raiz do projeto.

---

Rodar o container a partir da imagem criada
```
docker run hi-docker
```
> Executa um container com base na imagem `hi-docker`.

---

Listar todas as imagens Docker disponíveis
```
Docker images
```
> Exibe todas as imagens locais existentes no seu ambiente Docker.