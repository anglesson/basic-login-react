# Template Login App React

Template de Login para aplicações em React (Login sem redirecionamento).

## Instalação

Faça o clone da aplicação.
```bash
  git clone https://github.com/anglesson/basic-login-react.git
```

Entre no diretório da aplicação e instale as dependencias.

NPM:
```bash
  cd basic-login-react && npm install
```

Yarn:
```bash
  cd basic-login-react && yarn install
```
## Uso
Defina a URI de authenticação na função "loginUser" do arquivo "Login.js".
```js
async function loginUser(credentials) {
  return fetch("DEFINA_SUA_URI", {
    method: "POST",
    headers: {
      "Content-Type": "application/json",
    },
    body: JSON.stringify(credentials),
  }).then((data) => data.json());
}
```
<p style="color: red">
  Importante!
</p> Para este template a API de authenticação deve retornar o um token.

Formato de retorno:
```JS
{ token: ... }
```

## Funcionalidades
* Login
* Logout