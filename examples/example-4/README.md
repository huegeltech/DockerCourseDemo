# Arquivo: `index.html`

<!DOCTYPE html>
<html>
<head>
    <title>Minha App Docker!</title>
    <style>
        body { background: #1e1e1e; color: #fff; text-align: center; padding: 50px; }
        h1 { color: #4ec9b0; font-size: 2.5em; }
    </style>
</head>
<body>
    <h1>Primeira Pagina Docker!</h1>
    <p>Container funcionando!</p>
</body>
</html>


# Arquivo: `Dockerfile`

FROM nginx:alpine
COPY index.html /usr/share/nginx/html/
EXPOSE 80


# Construir imagem
docker build -t minha-pagina:v1.0 .


# Executar container
docker run -d -p 8080:80 --name meu-site minha-pagina:v1.0


# Teste: 
http://localhost:8080
