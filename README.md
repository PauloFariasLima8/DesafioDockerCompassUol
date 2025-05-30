# DesafioDockerCompassUol
 
*Paulo Farias Lima*


Abaixo segue os exercicios propostos no desafio de Docker do Programa de Bolsa de Estágio de DevSecOps da Compass Uol.

## Exercício 1.
1. Crie um arquivo Dockerfile que utilize a imagem alpine como base e
imprima a mensagem: "Olá, Docker!" ao ser executada. Construa a imagem
com o nome meu-echo e execute um container a partir dela. 

**1º. Passo: Instalar o Docker na máquina.**

Digite no seu terminal linux de base Debian:

 `sudo apt install docker.io -y`

**2º. Passo: Verificar se o docker foi instalado.**

Digite no seu terminal linux de base Debian:

`docker --version`

deve retornar algo como:
![](img/image1.png)

**3º. Passo: Criar o arquivo Dockerfile.**

Abra seu editor de texto prefencial e escreva o seguinte conteúdo:

```
FROM alpine:latest 
RUN echo "Criando a imagem"
CMD echo "Olá, Docker!"
```
Obs! O arquivo Dockerfile também está disponivel na pasta Exercicio1.

**4º. Passo: Salvar o arquivo Dockerfile e Buildar a imagem.**

Salve o arquivo como `Dockerfile` e execute o seguinte comando no terminal:

```
docker build -t meu-echo .
```
Deve retornar algo como:
![](img/image2.png)

**5º. Passo: Executar o container.**
Execute o seguinte comando no terminal:

```
sudo docker run meu-echo
```
Resultado esperado:

![](img/image3.png)

## Exercício 2.
Crie um container com Nginx que sirva uma página HTML customizada
(index.html). Monte um volume local com esse arquivo para que ele
apareça na raiz do site (/usr/share/nginx/html). Acesse a página via
http://localhost.

**1º. Passo: Criar o arquivo index.html.** 

Aqui sera reultilizado o index.html do desafio anterior do WebHook, os arquivos estão disponiveis na pasta Exercicio2.