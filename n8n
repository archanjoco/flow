# Vamos usar a imagem base do próprio N8N
FROM n8nio/n8n:latest

# para instalar o jq e o iputils, precisamos ser root
USER root

# Instala o jq e o iputils
RUN apk add --update jq iputils

# Volta para o usuário node que o n8n usa por padrão
USER node

# Cria a pasta nodes para instalar os community nodes
RUN mkdir ~/.n8n/nodes

################################
# Encontre nodes aqui:
# https://www.npmjs.com/search?q=keywords%3An8n-community-node-package
################################

# Instala o n8n-nodes-chatwoot
# https://www.npmjs.com/package/@sufficit/n8n-nodes-chatwoot
RUN cd ~/.n8n/nodes && npm i n8n-nodes-chatwoot

# Instala o n8n-nodes-text-manipulation
# https://www.npmjs.com/package/n8n-nodes-text-manipulation
RUN cd ~/.n8n/nodes && npm i n8n-nodes-text-manipulation

# Instala o n8n-nodes-cloudconvert
# https://www.npmjs.com/package/@cloudconvert/n8n-nodes-cloudconvert
RUN cd ~/.n8n/nodes && npm i @cloudconvert/n8n-nodes-cloudconvert

# Instala o n8n-nodes-randomizer
# https://www.npmjs.com/package/n8n-nodes-randomizer
RUN cd ~/.n8n/nodes && npm i n8n-nodes-randomizer

# Instala o n8n-quepasa
# https://www.npmjs.com/package/n8n-nodes-quepasa 
RUN cd ~/.n8n/nodes && npm i n8n-nodes-quepasa
