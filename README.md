# Simple Email Service Inspired by Uber

## Descrição
Este projeto implementa um serviço simples de envio de emails inspirado no sistema utilizado pela Uber. O serviço é desenvolvido em Java utilizando Spring Boot e é capaz de enviar emails através de uma interface RESTful. Ele é projetado para ser facilmente extensível e integrado com outras plataformas de envio de email, como AWS SES.

## Funcionalidades
- **Envio de Emails:** Envia emails utilizando uma API REST, passando os parâmetros `to`, `subject` e `body`.
- **Arquitetura Limpa:** Segue uma abordagem de Clean Architecture, onde a lógica de envio de email é separada em diferentes camadas (core, application, adapters).
- **Tratamento de Erros:** Implementa exceções personalizadas para tratamento de erros no envio de emails.

## Estrutura do Projeto

```plaintext
src/
  main/
    java/com/uber/email_service/
      adapters/
        EmailSenderGateway.java         # Interface para adaptar diferentes provedores de envio de email
      application/
        EmailSenderService.java         # Serviço que implementa a lógica de envio de email
      controllers/
        EmailSenderController.java      # Controlador REST que expõe a API de envio de email
      core/
        exception/
          EmailServiceException.java    # Exceções personalizadas para o serviço de email
        EmailRequest.java               # Classe que encapsula os dados do email a ser enviado
        EmailSenderUseCase.java         # Interface que define o caso de uso de envio de email
      infra/ses/
        AwsSesConfig.java               # Configurações específicas para integração com AWS SES (a ser implementado)
        SesEmailSender.java             # Implementação do adaptador para AWS SES (a ser implementado)
      EmailServiceApplication.java      # Classe principal que inicia a aplicação
    resources/
      application.properties            # Arquivo de configuração da aplicação
```

## Tecnologias Utilizadas
- **Java 17:** Linguagem de programação utilizada para desenvolver o serviço.
- **Spring Boot:** Framework que facilita a criação de aplicações Java robustas e escaláveis.
- **Maven:** Ferramenta de automação de build e gerenciamento de dependências.
- **AWS SES (opcional):** Serviço de envio de email da Amazon, utilizado como exemplo de integração com o projeto.

## Configuração e Execução

1. **Clone o repositório:**
   ```bash
   git clone https://github.com/rafaelnapolitanoo/API-Simple-Email-Service-Uber/edit/main/README.md```
   


