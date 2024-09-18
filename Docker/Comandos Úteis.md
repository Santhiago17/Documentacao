
## Comandos Essenciais para o Controle de Containers Docker

O Docker é uma plataforma poderosa para a criação e gerenciamento de containers, que são ambientes isolados para rodar aplicações. Para interagir com esses containers de forma eficiente, é fundamental conhecer os principais comandos.

**Comandos Básicos:**

- **docker run:** Cria um novo container a partir de uma imagem.

```bash
docker run -it my_image
```

-  `-i`: Permite interação com o terminal do container.
    - `-t`: Aloca um pseudo-TTY para o container.

- **docker ps:** Lista todos os containers em execução.

```bash
docker ps
```

**docker stop:** Para um container em execução.

```bash
docker stop container_id
```

**docker start:** Inicia um container parado.

```bash
docker start container_id
```

**docker rm:** Remove um container.

```bash
docker rm container_id

```

#### Gerenciando Imagens:

- **docker images:** Lista todas as imagens.

```bash
docker images
```

**docker pull:** Baixa uma imagem de um repositório.

```bash
docker pull ubuntu
```

**docker push:** Envia uma imagem para um repositório.

```bash
docker push my_repository/my_image
```

#### Interagindo com Containers:

- **docker exec:** Executa um comando dentro de um container em execução.

```bash
docker exec -it my_container bash
```

**docker logs:** Mostra os logs de um container.

```bash
docker logs my_container
```

#### Gerenciando Volumes:

- **docker volume create:** Cria um volume.

```bash
docker volume create my_volume
```

**docker volume rm:** Remove um volume.

```bash
docker volume rm my_volume
```

#### Outros Comandos Úteis:

- **docker inspect:** Exibe detalhes sobre um container ou imagem.

```bash
docker inspect my_container
```

**docker system prune:** Remove containers não utilizados, imagens pendentes, redes não utilizadas e volumes não utilizados.

```bash
docker system prune -a
```

#### Exemplos Práticos:

- **Criar um container Ubuntu interativo:**

```bash
docker run -it ubuntu bash
```

**Rodar um servidor web Nginx:

```bash
docker run -d -p 80:80 nginx
```

**Copiar um arquivo para dentro de um container:

```bash
docker cp meu_arquivo.txt my_container:/home/user
```

**Docker stats: Monitora estatísticas de recursos de containers em tempo real.

```bash
docker stats
```
**Docker prune -a: Remove todos os recursos não utilizados (containers, imagens, redes, volumes, etc.).

```bash
docker system prune -a
```

**Criar um container Node.js com volumes:

```bash
docker run -d -p 3000:3000 -v $(pwd):/app node my-app
```

**Dicas Adicionais:**

- **Dockerfile:** Um arquivo de texto que contém todos os comandos necessários para criar uma imagem Docker.
- **Docker Compose:** Uma ferramenta para definir e executar aplicações multi-container usando um único arquivo YAML.
- **Redes Docker:** Crie redes personalizadas para conectar seus containers.

