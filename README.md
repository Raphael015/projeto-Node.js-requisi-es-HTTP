# Projeto Node.js - responder requisições HTTP.

## Para começar, siga os passos abaixo.

1. **Certifique-se de ter o Node.js instalado no seu sistema.**

   Se você ainda não tem o Node.js instalado, você pode baixá-lo [aqui](https://nodejs.org/). Escolha a versão recomendada para a sua plataforma e siga as instruções de instalação.

2. Crie um novo arquivo chamado `server.js`.

3. Copie e cole o seguinte código no arquivo `server.js`:

    ```javascript
    // Importa o módulo HTTP interno do Node.js
    const http = require('http');

    // Configurações do servidor
    const hostname = '127.0.0.1';
    const port = 3000;

    // Cria um servidor HTTP
    const server = http.createServer((req, res) => {
      // Configura o cabeçalho da resposta
      res.statusCode = 200;
      res.setHeader('Content-Type', 'text/plain');
      
      // Envia a resposta
      res.end('Olá, mundo!\n');
    });

    // Inicia o servidor para escutar as requisições HTTP
    server.listen(port, hostname, () => {
      console.log(`Servidor rodando em http://${hostname}:${port}/`);
    });
    ```

4. Salve o arquivo.

5. Agora, para rodar e testar o servidor:

   - Abra o prompt de comando (cmd) no diretório onde o arquivo `server.js` está localizado.

   - Execute o seguinte comando para iniciar o servidor:

     ```bash
     node server.js
     ```

   - Isso iniciará o servidor na porta 3000.

   - Abra um navegador da web e acesse [http://127.0.0.1:3000/](http://127.0.0.1:3000/) ou [http://localhost:3000/](http://localhost:3000/). Você deve ver a mensagem "Olá, mundo!".

   - Para encerrar o servidor, volte ao prompt de comando e pressione Ctrl + C.
