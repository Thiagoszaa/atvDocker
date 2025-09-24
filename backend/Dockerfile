# Usa a imagem base do Node.js
FROM node:18-alpine

# Define o diretório de trabalho
WORKDIR /usr/src/app

# Copia os arquivos de definição de pacotes e instala as dependências
COPY package*.json ./
RUN npm install

# Copia o código-fonte
COPY . .

# Expõe a porta que a aplicação NestJS usará
EXPOSE 3000

# Comando para iniciar a aplicação em modo de desenvolvimento
CMD ["npm", "run", "start:dev"]