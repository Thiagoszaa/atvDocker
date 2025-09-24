# Imagem base do Node
FROM node:lts-alpine

# Define o diretório de trabalho
WORKDIR /usr/src/app

# Copia os arquivos de definição de dependências
COPY package*.json ./

# Instala as dependências
RUN npm install

# Copia o restante do código da aplicação
COPY . .

# Expõe a porta que o Vite utiliza
EXPOSE 5173

# Comando para iniciar o servidor de desenvolvimento do Vite
# O host 0.0.0.0 é necessário para expor a aplicação fora do container
CMD ["npm", "run", "dev", "--", "--host", "0.0.0.0"]