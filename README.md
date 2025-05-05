# API-de-Pagamentos-Segura-com-Azure-API-Management

API de Pagamentos com Segurança e Controle de Acesso no Azure
Desenvolvi um projeto focado na criação de uma API para pagamentos, com ênfase na segurança, escalabilidade e gerenciamento de acesso, utilizando os principais serviços da Microsoft Azure.

A arquitetura foi construída pensando na proteção dos dados sensíveis e na exposição segura da API para consumidores externos. Para isso, usei o Azure API Management como ponto central para publicar, proteger e monitorar a API. Ele atua como um gateway, aplicando políticas de segurança, limites de requisições e exigindo chaves de assinatura ou tokens JWT.

Para controle de identidade e autenticação, integrei com o Microsoft Entra ID (Azure AD), garantindo que apenas usuários e aplicativos autorizados possam consumir os endpoints. Também explorei o uso de Azure Key Vault para armazenar segredos, como chaves de criptografia e tokens de acesso, sem expô-los no código.

A API em si foi hospedada como um App Service com HTTPS obrigatório e acesso restrito via IP, enquanto os logs e métricas de uso ficaram centralizados no Azure Monitor e Application Insights, o que ajudou bastante na observabilidade e diagnóstico.

Esse projeto me permitiu entender na prática como usar os recursos da Azure para entregar uma API robusta, segura e com controle total de acesso, algo essencial em cenários financeiros e de pagamento digital.

Exercise 1: Create an Azure App Service resource by using a Docker container image

![Image](https://github.com/user-attachments/assets/9c1f5f59-2603-4170-a6cd-9119dd55b0b2)

*Create a web app by using Azure App Service resource by using an httpbin container image

![Image](https://github.com/user-attachments/assets/11480a10-182c-40ce-81f1-562d18b765ec)

*Test the httpbin web application

![Image](https://github.com/user-attachments/assets/d6c79e9e-5bcc-4fd0-be56-2b278a876274)

*Build an API proxy tier by using Azure API Management

![Image](https://github.com/user-attachments/assets/37102300-dbce-4654-80c8-639bb43bc8f9)

**Define a new API

![Image](https://github.com/user-attachments/assets/39e431e9-1af7-4c75-909a-ea25b0bc5386)

*On the Design tab, select + Add operation.

![Image](https://github.com/user-attachments/assets/4e34d260-7340-494a-9a3d-565899144dc5)

*Inbound processing 

![Image](https://github.com/user-attachments/assets/9b3bb850-fa97-4784-b517-592898d1e885)

*section for Echo Headers, on the Backend tile, select the pencil icon.

![Image](https://github.com/user-attachments/assets/eb3e3a92-a140-4795-b4da-caff0555ef34)

 *list of operations, select Echo Headers, and then select the Test tab.

 ![Image](https://github.com/user-attachments/assets/90337858-c32c-466f-bf56-f5f282e40318)

 *The following screenshot displays the response to the Echo Headers request.

 ![Image](https://github.com/user-attachments/assets/d41f0f18-9102-4012-a45c-823fa18bb81c)

 *list of operations, select Get Legacy Data.

 ![Image](https://github.com/user-attachments/assets/cd8a878f-a14a-4bf1-b915-01a2538af4f2)

 * select Modify Status Code.

 ![Image](https://github.com/user-attachments/assets/9d05272a-ed1b-49c2-a6cb-471ca39634ed)

* on the Inbound processing tile, select + Add policy.

![Image](https://github.com/user-attachments/assets/75bd45ed-6e7a-4d5f-b4e0-fe7dedae9073)

*select Modify Status Code, and then select the Test tab.

![Image](https://github.com/user-attachments/assets/0049c7ce-caec-4ffa-84e3-ebdc203755ec