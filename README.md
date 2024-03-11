# Google Sign-In with jwt-decode

Este projeto demonstra como implementar o login do Google em uma página da web usando a API Google Sign-In. Além disso, ele utiliza a biblioteca jwt-decode para decodificar informações do token JWT recebido após o login.

## Pré-requisitos

Antes de começar, certifique-se de ter uma conta de desenvolvedor no Google Cloud Console, onde você pode criar um projeto e obter o ID do cliente necessário.

##  Configuração

 1 Clone o repositório ou copie o código HTML para o seu projeto

 2  Substitua o valor de client_id na função google.accounts.id.initialize pelo ID do cliente obtido no Console do Google Cloud.

 ```javascript 
 client_id: "SEU_ID_DO_CLIENTE_AQUI",
 ```

3 Certifique-se de que a biblioteca jwt-decode está sendo carregada corretamente. O código atual usa a versão 3.1.2, mas você pode verificar aqui para obter a versão mais recente.

```html 
<script src="https://unpkg.com/jwt-decode@3.1.2/build/jwt-decode.js"></script>
```

## Uso 
1 Abra o arquivo HTML em um navegador da web.
2 Clique no botão "Continue with Google" para iniciar o processo de login do Google.
3 Após o login bem-sucedido, as informações do usuário serão exibidas na página.

## Estrutura do Código

- handleCredentialResponse: Função que manipula a resposta de credenciais do Google, decodifica o token JWT e atualiza os elementos HTML com informações do usuário.

- window.onload: Evento que é acionado quando a janela está totalmente carregada. Inicializa o Google Sign-In, renderiza o botão de login e exibe o diálogo "One Tap".
