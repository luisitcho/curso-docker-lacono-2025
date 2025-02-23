# syntax=docker/dockerfile:1

FROM node:lts-alpine

# Define o diretório de trabalho dentro do contêiner
WORKDIR /app

# Cria um grupo e um usuário para executar a aplicação
# RUN addgroup dev && adduser -S -G luisitcho dev

# Muda para o usuário recém-criado para maior segurança
# USER luisitcho

# Copia apenas o package.json para instalar dependências primeiro (boa prática de cache)
COPY package.json ./

# Instala as dependências de produção
RUN apk add --no-cache python3 g++ make && yarn install --production

# Expõe a porta 3000 para acesso externo
EXPOSE 3000

# Copia o restante dos arquivos da aplicação para o diretório de trabalho
COPY . .

# Define o comando que será executado quando o contêiner iniciar
CMD ["node", "src/index.js"]