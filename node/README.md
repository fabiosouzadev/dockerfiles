# Exemplo Node+Express
> Exemplo compartilhando pasta pra desenvolvimento

Para compartilhar a pasta atual dento do container 

```bash
docker run --rm -it -v $(pwd):/usr/src/app -p 3000:3000 node:19 bash
```
assim é possivel mudar os arquivos e ver as mudanças no container.


Depois disso, basta rodar dentro do container

```bash
yarn init
node index.js
```

 
