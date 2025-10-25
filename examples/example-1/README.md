# Criar conteúdo
mkdir -p meu-site


# Gere o html
echo '<h1>Meu Primeiro Docker!</h1><p>Site funcionando!</p>' > meu-site/index.html


# Servir conteúdo personalizado
docker run -d -p 8080:80 --name meu-site -v $(pwd)/meu-site:/usr/share/nginx/html nginx:alpine


# Teste: 
http://localhost:8080