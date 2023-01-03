# Desafio - Descreva o uso do Cloud Shell e Execute uma aplicação exemplo

Para demonstração deste desafio, será feito o clone do projeto “**quarkus-helloworld** ” presente no Github oficial do Google Cloud Plataform presente no seguinte [repositório.](https://github.com/GoogleCloudPlatform/java-docs-samples/tree/main/appengine-java11/quarkus-helloworld)

### Como acessar o Cloud Shell?

<a href="https://console.cloud.google.com/cloudshell/open?git_repo=https://github.com/GoogleCloudPlatform/java-docs-samples&page=editor&open_in_editor=appengine-java11/README.md">
<img alt="Open in Cloud Shell" src ="http://gstatic.com/cloudssh/images/open-btn.png"></a>

- Após fazer o login em seu console GCP, clique no botão **“Ativar o Cloud Shell”** do lado direito na barra superior;
    - Assim que clicar no botão será feito a configuração inicial e inicialização do Cloud Shell.
    - Quando o Cloud Shell for inicializado, você poderá fazer o uso de comandos/execução de scipts diretamente por esta interface.


![img-01-acessando o cloudshell](https://user-images.githubusercontent.com/32373902/210443255-d5f0065f-948e-44ed-af31-7393d0fae97e.png)

### Executar um projeto no Cloud Shell

- Os comandos do Cloud Shell utiliza a mesma sintaxe de sistemas baseados em Shell-Linux
    - Primeiro comando para se executar é o `git clone` no projeto
    
               git clone https://github.com/GoogleCloudPlatform/java-docs-samples.git
               
   ![img-03-clone-do-projeto-no-shell](https://user-images.githubusercontent.com/32373902/210443261-0798bff5-f861-4a19-8164-8369428b9ebb.png)
   ![img-04-clone-do-projeto-no-shell-finalizado](https://user-images.githubusercontent.com/32373902/210443264-a0037198-c47f-43e6-b207-2fd4cffeddef.png)
    - Após o a conclusão do projeto podemos executar de duas formas:
        1. Executar todos os códigos via CLI 
        2. Ter ajuda de outra ferramenta para aprimorar nossa experiência: **Cloud Shell Editor**
            1. **Essa será a alternativa utilizada**
            
    - Para abrir o editor, basta clicar no botão **“📝abrir editor“**
    ![img-05-opencloudshell](https://user-images.githubusercontent.com/32373902/210443265-9a9c6a7d-37a6-41d4-9052-87050089ac66.png)
        - Aguarde a inicialização
        ![img-06-opencloudshell](https://user-images.githubusercontent.com/32373902/210443267-dd6175a3-cfb0-46d2-8570-f5edacbac043.png)
        - O Editor Cloud Shell mostrará duas diferentes ambientes
        ![img-07-opencloudshell](https://user-images.githubusercontent.com/32373902/210443269-05184d73-d557-4fc6-a612-7d02e21aae39.png)
            - O ambiente dos **“explorer”** onde será mostrado todas as informações de diretórios em seu **GCP**
            - O ambiente de **IDE** para edição dos códigos
                - Na IDE podemos abrir um terminal para executar nossos comandos
                    - Vamos abrir a pasta do projeto → Acessar o diretório ************************************appengine-java11************************************ → acessar o diretório quarkus-helloworld.
                        - Acesse o menu **Terminal → New Terminal**
                        ![img-08](https://user-images.githubusercontent.com/32373902/210443272-fe78c6a5-c050-4587-b6c8-4dd838c23930.png)

                    - Instalar o **Maven** em nosso projeto
                    
               **Para acessar nosso projeto:**
                
                ```bash
                cd java-docs-samples
                cd appengine-java11
                cd quarkus-helloworld
                
                #instale o Maven no diretório: 
                mvn clean install 
                
                # aguarde a instalação 
                ```
                
                - Você pode navegar diretamente pelo menu **explorer** e encontrar o diretório diretamente, clique com o botão direito no diretório do projeto e “**Open in Terminal”,** assim, será aberto um terminal exatamente no diretório selecionado
            ![img-09](https://user-images.githubusercontent.com/32373902/210443276-71331952-5b31-46d4-b90d-0eb9437785a0.png)
            ![img-09-1](https://user-images.githubusercontent.com/32373902/210443277-0ec257fb-1958-48c0-a29a-08af045633b8.png)

            ### Analisando dependências:
            
            - A ferramenta é altamente completa e analisa diretamente as dependências do projeto percebendo diretamente qual a linguagem será executada.
            
            ![img-10](https://user-images.githubusercontent.com/32373902/210443279-25a6d448-c391-4a3f-a170-16d25ab007a0.png)

            
            Para execução do seu código use o comando: 
            
            `java -jar quarkus-helloworld-1.0-SNAPSHOT-runner.jar`
            
             - O quarkus será iniciado diretamente na porta **8080**
            ![Screenshot_11](https://user-images.githubusercontent.com/32373902/210443281-6c79be48-270b-47c9-821f-c825aeff0386.png)

            - Você poderá clicar diretamente na opção “Visualização na Web” e assim abrir uma nova janela no navegador para acessar a aplicação.
            - É possível alterar a porta de acesso a sua aplicação.
         
            ![Screenshot_12](https://user-images.githubusercontent.com/32373902/210443282-233e45f8-50fe-4b26-9bdf-10f6c35f9ae0.png)
            
            
 Assim, sua aplicação será mostrada no navegador, no caso, um exemplo **“Hello World!”**

![Screenshot_13](https://user-images.githubusercontent.com/32373902/210443284-a4d233cd-c1dd-4442-86d1-b14a5681946f.png)



## Outra forma é utilizando a CLI para realizar um Deploy

Use o comando:

```bash
gcloud app deploy
```
Execute as configurações utilizando CLI

Para verificar a sua aplicação, use o comando:
```
gcloud app browse
```
Ou navegue por `https://<your-project-id>.appspot.com`.

Esse modo irá criar uma nova instancia de aplicação em seu "App Engine"
