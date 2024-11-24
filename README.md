

[![Link Bio](https://img.shields.io/badge/Link%20Bio-59d959?style=for-the-badge&logo=about.me&logoColor=white)](https://santosqa.github.io) [![About](https://img.shields.io/badge/About.me-993399?style=for-the-badge&logo=about.me&logoColor=white)](https://about.me/santosqa) [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/santosqa) [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/santosqa) [![Instagram](https://img.shields.io/badge/instagram-%23E4405F.svg?&style=for-the-badge&logo=instagram&logoColor=white)](https://www.instagram.com/santosqa_/) [![Santos QA](https://img.shields.io/badge/SantosQA.COM-BD93F9?style=for-the-badge&logo=twitter&logoColor=white)](https://santosqa.com/) [![Apartamento Vista Mar](https://img.shields.io/badge/ApartamentoVistaMar.com-FFB86C?style=for-the-badge&logo=twitter&logoColor=white)](https://www.apartamentovistamar.com/)


## 💻 O Projeto

 Repositorio de exemplo para uso do curso Datadog Power User da appoena.
  
  - **Conheça a Appoena em:**
  ``` https://appoena.com.br/ ```

  - **Repositorio Original da Appoena:**
    ``` https://github.com/appoena/datadogpoweruser ```


### Comando usado dentro da pasta/projeto desejado. neste exemplo estou usando o ```/apm/dotnet```:
  1. Instalação do minikube no mac: ( caso já tenha instalado, pode ser ignorado )
    ``` brew install minikube ```
  2. Ininciando o minikube:
    ``` minikube start --driver=docker ```
  3. Buildando a aplicação: ( !necessário que o docker já esteja rodando, pois será criado uma imagem nele )
    ``` docker build . -t dotnet-todoapi ```
  4. Iniciando imagem:
    ``` docker run -d -p 8081:80 --name dotnet-todoapi dotnet-todoapi ```
  5. Fazendo deploy da aplicação: 
    ``` kubectl apply -f dotnet-todoapi.yaml ```
    Ou
    ``` docker build -t dotnet-todoapi . ```
  6. Verificar os pods em execução
    ``` kubectl get pods ```
  7. Verificar o status do serviço:
    ``` kubectl get svc ```
  8. Iniciando tunel para acesso externo:
    ``` minikube tunnel ```
  9. Rodar aquivo para popular dados:
    ``` ./populate.sh ```



# Demais comandos úteis

## Instalação do Docker no Minikube no mac (certifique de ter o docker já instalado)
  ``` brew install minikube ``` 

  Inicie o Minikube usando Docker como driver:
  ``` minikube start --driver=docker ``` 

  Verifique o status:
  ``` minikube status ``` 

# Comandos úteis para o dia a dia:

### Acessar o dashboard do Kubernetes
 ``` minikube dashboard ``` 

### Obter o IP do cluster
 ``` minikube ip ``` 

### Parar o cluster
 ``` minikube stop ``` 

### Deletar o cluster
 ``` minikube delete ``` 

### Listar addons disponíveis
 ``` minikube addons list ``` 

### Habilitar um addon (exemplo: metrics-server)
 ``` minikube addons enable metrics-server ``` 

# Para implantar uma aplicação de exemplo:
# Criar um deployment
 ``` kubectl create deployment hello-minikube --image=kicbase/echo-server:1.0 ``` 

# Expor o serviço
 ``` kubectl expose deployment hello-minikube --type=NodePort --port=8080 ``` 

# Obter a URL do serviço
 ``` minikube service hello-minikube --url ``` 


# Para usar imagens Docker locais com Minikube:

### Aponte o Docker CLI para o daemon Docker do Minikube
 ``` eval $(minikube docker-env) ``` 

### Para voltar ao Docker local
 ``` eval $(minikube docker-env -u) ``` 

### Para acessar o registro de logs:
 ``` minikube logs ``` 

### Para aumentar os recursos alocados ao cluster:
 ``` minikube start --driver=docker --cpus=4 --memory=8192 ``` 




---

 [Ricardo Santos QA](https://github.com/santosqa) 👋🏼