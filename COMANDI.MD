docker compose down && docker compose up -d

docker compose up -d --build mirofish

Per quelle modifiche serve rebuild del container mirofish:

docker compose down
docker compose build mirofish
docker compose up -d


docker compose logs -f
docker logs mirofish-ollama --tail 1000

docker exec mirofish-ollama ollama pull qwen2.5:14b