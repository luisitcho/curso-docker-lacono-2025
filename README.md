# 🚀 Docker do Básico ao Avançado  

Este repositório contém materiais práticos sobre Docker, abordando:  

- Conceitos básicos de containers  
- Instalação do Docker em diferentes sistemas operacionais  
- Criação e personalização de imagens  
- Gerenciamento de containers, volumes e redes  
- Uso do Docker Compose para aplicações multicontainer  
- Testes e debugging dentro de containers  
- Implantação de aplicações em produção  
- Integração do Docker com pipelines CI/CD  

<h2>Comandos do Dockerfile</h2>
<ul>
    <li><strong>FROM</strong> - Define a imagem base.<br>
        Exemplo: <code>FROM ubuntu:latest</code></li>
    <li><strong>RUN</strong> - Executa comandos no contêiner durante a construção.<br>
        Exemplo: <code>RUN apt-get update && apt-get install -y nginx</code></li>
    <li><strong>COPY</strong> - Copia arquivos do host para o contêiner.<br>
        Exemplo: <code>COPY index.html /usr/share/nginx/html/</code></li>
    <li><strong>ADD</strong> - Copia arquivos do host ou de uma URL para o contêiner, podendo descompactar arquivos.<br>
        Exemplo: <code>ADD arquivo.tar.gz /app/</code> ou <code>ADD https://url.do/arquivo.ext /caminho/para/o/</code></li>
    <li><strong>WORKDIR</strong> - Define o diretório de trabalho.<br>
        Exemplo: <code>WORKDIR /app</code></li>
    <li><strong>CMD</strong> - Define o comando padrão a ser executado.<br>
        Exemplo: <code>CMD ["nginx", "-g", "daemon off;"]</code></li>
    <li><strong>ENTRYPOINT</strong> - Define o comando principal do contêiner.<br>
        Exemplo: <code>ENTRYPOINT ["python", "app.py"]</code></li>
    <li><strong>EXPOSE</strong> - Expõe uma porta do contêiner.<br>
        Exemplo: <code>EXPOSE 80</code></li>
    <li><strong>ENV</strong> - Define variáveis de ambiente.<br>
        Exemplo: <code>ENV PORT=8080</code></li>
    <li><strong>VOLUME</strong> - Define um volume para persistência de dados.<br>
        Exemplo: <code>VOLUME /app/data</code></li>
</ul>

<h2>Comandos Úteis do Docker</h2>
<ul>
    <li><strong>docker build</strong> - Cria uma imagem a partir de um Dockerfile.<br>
        Exemplo: <code>docker build -t minha-imagem .</code></li>
    <li><strong>docker run</strong> - Executa um contêiner baseado em uma imagem.<br>
        Exemplo: <code>docker run -d -p 80:80 minha-imagem</code></li>
    <li><strong>docker ps</strong> - Lista os contêineres em execução.</li>
    <li><strong>docker ps -a</strong> - Lista todos os contêineres, incluindo os parados.</li>
    <li><strong>docker images</strong> - Lista todas as imagens disponíveis.</li>
    <li><strong>docker rm</strong> - Remove um contêiner.<br>
        Exemplo: <code>docker rm meu-container</code></li>
    <li><strong>docker rmi</strong> - Remove uma imagem.<br>
        Exemplo: <code>docker rmi minha-imagem</code></li>
    <li><strong>docker stop</strong> - Para um contêiner em execução.<br>
        Exemplo: <code>docker stop meu-container</code></li>
    <li><strong>docker logs</strong> - Exibe os logs de um contêiner.<br>
        Exemplo: <code>docker logs meu-container</code></li>
    <li><strong>docker exec</strong> - Executa um comando dentro de um contêiner em execução.<br>
        Exemplo: <code>docker exec -it meu-container /bin/bash</code></li>
    <li><strong>docker volume create</strong> - Cria um volume.<br>
        Exemplo: <code>docker volume create meu-volume</code></li>
    <li><strong>docker volume ls</strong> - Lista todos os volumes.</li>
    <li><strong>docker volume inspect</strong> - Exibe detalhes sobre um volume.<br>
        Exemplo: <code>docker volume inspect meu-volume</code></li>
    <li><strong>docker volume rm</strong> - Remove um volume.<br>
        Exemplo: <code>docker volume rm meu-volume</code></li>
    <li><strong>docker run -v</strong> - Monta um volume em um contêiner.<br>
        Exemplo: <code>docker run -d -v meu-volume:/app/data minha-imagem</code></li>
</ul>
