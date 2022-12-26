# Laravel (PHP-FPM) + NGINX (Proxy Reverso)

> Exemplo de um Dockerfile de build usando [Laravel](https://laravel.com/) com [PHP-FPM](https://www.php.net/manual/pt_BR/install.fpm.php) e [NGINX](https://www.nginx.com/) como proxy reverso

### 📋 Pré-requisitos

* [Docker](https://www.docker.com/)

## 🛠️ Build imagem com Laravel
```bash
docker build -t laravel-prod ../laravel/ -f ../laravel/Dockerfile.prod
```

## 🛠️ Build imagem com nginx
```bash
docker build -t nginx-prd . -f Dockerfile.prod
```

## Criar uma network para comunicação dos dois servicos
```bash
docker network create laravel-network
```

## Criar container á partir da imagem laravel
```bash
docker run -d --network laravel-network --name laravel laravel-prod
```

## Criar container á partir da imagem laravel
```bash
docker run -d --network laravel-network --name nginx -p 8080:80 nginx-prd
```
