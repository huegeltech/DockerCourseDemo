## ❌ Problema: Dados Perdidos

docker run -d --name meu-banco -e POSTGRES_PASSWORD=senha123 postgres:13
docker exec -it meu-banco createdb -U postgres meu_app_senac
docker exec -it meu-banco psql -U postgres -l    # Listar bases criadas
docker rm -f meu-banco  # 💀 Dados perdidos!


## ✅ Solução: Volumes

# Opção 1: Volume nomeado (Docker gerencia)
docker volume create meus-dados
docker run -d \
  --name meu-banco \
  -e POSTGRES_PASSWORD=senha123 \
  -v meus-dados:/var/lib/postgresql/data \
  postgres:13


# Opção 2: Mapeamento direto para pasta específica
mkdir -p $(pwd)/data/postgresql
docker run -d \
  --name meu-banco \
  -e POSTGRES_PASSWORD=senha123 \
  -v $(pwd)/data/postgresql:/var/lib/postgresql/data \
  postgres:13
