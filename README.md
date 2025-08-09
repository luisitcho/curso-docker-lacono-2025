# Docker do Básico ao Avançado

Este repositório contém materiais práticos e objetivos sobre Docker, abordando desde os conceitos iniciais até práticas avançadas para uso em produção.

* Arquivo com os comandos mais importantes: [docker-cheat-sheet](https://github.com/luisitcho/curso-docker-lacono-2025/blob/main/docker-cheat-sheet.pdf)
* [Certificado de conclusão](https://www.udemy.com/certificate/UC-c1071bbb-0321-4da5-899b-94ab7584a144/)

## Tópicos Abordados
- Conceitos básicos de containers  
- Instalação do Docker em diferentes sistemas operacionais  
- Criação e personalização de imagens  
- Gerenciamento de containers, volumes e redes  
- Uso do Docker Compose para aplicações multicontainer  
- Testes e debugging dentro de containers  
- Implantação de aplicações em produção  
- Integração do Docker com pipelines CI/CD  

---

## Comandos do **Dockerfile**

### `FROM`
Define a imagem base para a construção do container.  
**Exemplo:**
```dockerfile
FROM ubuntu:latest
```

### `RUN`
Executa comandos no container durante o processo de build.  
**Exemplo:**
```dockerfile
RUN apt-get update && apt-get install -y nginx
```

### `COPY`
Copia arquivos do host para dentro do container.  
**Exemplo:**
```dockerfile
COPY index.html /usr/share/nginx/html/
```

### `ADD`
Copia arquivos do host ou de uma URL para dentro do container, com suporte a descompactação automática.  
**Exemplo:**
```dockerfile
ADD arquivo.tar.gz /app/
ADD https://url.do/arquivo.ext /destino/
```

### `WORKDIR`
Define o diretório de trabalho padrão para os comandos subsequentes.  
**Exemplo:**
```dockerfile
WORKDIR /app
```

### `CMD`
Define o comando padrão a ser executado quando o container for iniciado (pode ser sobrescrito).  
**Exemplo:**
```dockerfile
CMD ["nginx", "-g", "daemon off;"]
```

### `ENTRYPOINT`
Define o comando principal que sempre será executado no container.  
**Exemplo:**
```dockerfile
ENTRYPOINT ["python", "app.py"]
```

### `EXPOSE`
Informa qual porta o container expõe para comunicação.  
**Exemplo:**
```dockerfile
EXPOSE 80
```

### `ENV`
Define variáveis de ambiente dentro do container.  
**Exemplo:**
```dockerfile
ENV PORT=8080
```

### `VOLUME`
Define pontos de montagem para persistência de dados.  
**Exemplo:**
```dockerfile
VOLUME /app/data
```

---

## 🔧 Comandos Úteis do Docker

### Criar uma imagem a partir de um Dockerfile
```bash
docker build -t minha-imagem .
```

### Executar um container
```bash
docker run -d -p 80:80 minha-imagem
```

### Listar containers
```bash
docker ps        # Apenas containers em execução
docker ps -a     # Todos os containers (incluindo parados)
```

### Listar imagens
```bash
docker images
```

### Remover container
```bash
docker rm meu-container
```

### Remover imagem
```bash
docker rmi minha-imagem
```

### Parar container
```bash
docker stop meu-container
```

### Ver logs de um container
```bash
docker logs meu-container
```

### Executar comando dentro de um container
```bash
docker exec -it meu-container /bin/bash
```

### Criar volume
```bash
docker volume create meu-volume
```

### Listar volumes
```bash
docker volume ls
```

### Inspecionar volume
```bash
docker volume inspect meu-volume
```

### Remover volume
```bash
docker volume rm meu-volume
```

### Montar volume ao criar container
```bash
docker run -d -v meu-volume:/app/data minha-imagem
```

---

> ⚠️ Nota: Sempre nomeie containers, imagens e volumes de forma clara para facilitar manutenção e automação.
