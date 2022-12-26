# Laravel

> Exemplo de um Dockerfile para desenvolvimento usando [Laravel](https://laravel.com/)

### 📋 Pré-requisitos

* [Docker](https://www.docker.com/)

## 🛠️ Como fazer o build esse Dockerfile
```bash
docker build -t {nome-da-imagem} .
```

## Como criar containers à partir dessa imagem
```bash
docker run -dit --rm --name {nome-do-container} -p 8080:8080 {nome-da-imagem}
```

## Como criar containers à partir dessa imagem
```bash
docker run -dit --rm --name {nome-do-container} -p 8080:8080 {nome-da-imagem}
```

## Como criar containers à partir dessa imagem trocando host ou port
```bash
docker run -dit --rm --name {nome-do-container} -p 8081:8081 {nome-da-imagem} --host=0.0.0.0 --port=8081
```

