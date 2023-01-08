# Docker To Do List 🐳

## 📄 Sobre:

Projeto desenvolvido durante o módulo de back-end do curso de desenvolvimento web da [Trybe](https://www.betrybe.com/).

Neste projeto foram criados containers para uma aplicação full stack préviamente desenvolvida.

Os objetivos principais do projetos eram:
> * Conteinerizar as aplicações
> * Criar uma conexão entre elas
> * Orquestrar seu funcionamento

Para o desenvolvimento do projeto foram utilizados os comandos CLI do docker, Dockerfile e Docker-Compose.

</br>
<details>
<summary><strong>Desempenho</strong></summary>
Aprovado com 100% de desempenho em todos os requisitos

![image](https://user-images.githubusercontent.com/99846604/211217996-3a3c33b2-83e9-4ed0-95fe-be120f60ec89.png)

</details>

<details>
<summary><strong>Requisitos</strong></summary>
</br>
<strong>Requisitos obrigatórios:</strong> </br>

</br>
Comandos docker: </br>
1. Crie um container em modo interativo, sem rodá-lo, nomeando-o como "01container" e utilizando a imagem "alpine" na versão "3.12" </br>
2. Inicie o container "01container" </br>
3. Liste os containers filtrando pelo nome "01container" </br>
4. Execute o comando "cat /etc/os-release" no container "01container" sem se acoplar a ele </br>
5. Remova o container "01container" </br>
6. Faça o download da imagem "nginx" com a versão "1.21.3-alpine" sem criar ou rodar um container </br>
7. Rode um novo container com a imagem  "nginx" com a versão "1.21.3-alpine" em segundo plano nomeando-o como "02images" e mapeando sua porta padrão de acesso para porta "3000" do sistema hospedeiro </br>
8. Pare o container "02images" que está em andamento </br>
</br>

Dockerfile: </br>
9. Gere uma build a partir do Dockerfile do "back-end" do "todo-app" nomeando a imagem para "todobackend" </br>
10. Gere uma build a partir do Dockerfile do "front-end" do "todo-app" nomeando a imagem para "todofrontend" </br>
11. Gere uma build a partir do Dockerfile dos "testes" do "todo-app" nomeando a imagem para "todotests" </br>

<strong>Requisitos bônus:</strong> </br>

Docker-compose: </br>
12. Suba uma orquestração em segundo plano com o docker-compose de forma que "backend", "frontend" e "tests" consigam se comunicar </br>
</details>
</br>

## ⚙️ Execução

Para executar a aplicação inicie realizando o clone deste repositório com o comando abaixo.

    git clone git@github.com:joaoespacheco/Trybe-Project-21-Docker-To-Do-List.git
    
Navegue até o diretório **docker** do projeto.

    cd docker-todo-list/docker

<details>
   <summary><strong>Rodando a aplicação com o Docker</strong></summary> 
  </br>
  
  <strong>Obs:</strong> Para rodar a aplicação dessa forma você deve ter o [Docker](https://www.docker.com/) instalado na sua máquina.
  
  </br>
  
  Instale as dependências do projeto na pasta back-end, fornt-end e tests rodando o comando abaixo dentro de cada pasta

        npm install
  
  Na pasta docker do projeto, suba o container <strong>todofront</strong>, <strong>todoback</strong> e <strong>todotests</strong> utilizando o docker-compose.yml. 
  
Utilize o comando abaixo.

        docker-compose up -d

Entre no terminal do container de back-end com o comando:

        docker exec -it docker-todoback-1 bin/sh

Dentro do terminal, inicie o servidor

        npm run dev
        
 Entre no terminal do container de front-end com o comando:
    
        docker exec -it docker-todofront-1 bin/sh
        
 Inicie a aplicação react com o comando abaixo dentro do terminal do container
    
        npm start

 Entre no terminal do container de tests com o comando:
    
        docker exec -it docker-todotests-1 bin/sh
        
 Inicie a execução dos testes com o comando:
    
        npm test

</details>
<br/>

## 🤹🏽 Habilidades Desenvolvidas:
* Utilizar a CLI do Docker para executar comandos
* Criar imagens com Dockerfile
* Rodar múltiplos containers utilizando o Docker-Compose

</br>

## 🧰 Ferramentas:
* Docker
  * Docker Hub
  * Docker Compose
</br>

## 📝 Desenvolvido por:
* [João Emanuel Soares Pacheco](https://github.com/joaoespacheco)
