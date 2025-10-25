# Criar pasta permanente
mkdir -p meu-site


# Gere o html
echo '<h1>Meu Site Persistente</h1><p>Editavel!</p>' > meu-site/index.html


# Container com volume persistente
docker run -d --name meu-site \
  -p 8080:80 \
  -v $(pwd)/meu-site:/usr/share/nginx/html \
  nginx:alpine


# Editar arquivo (site muda instantaneamente!)
echo '<h1>Site Atualizado \o/ !</h1><p>\o/</p>' > meu-site/index.html


# Teste: 
http://localhost:8080
