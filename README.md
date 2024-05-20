<img src="https://ibb.co/xsxs2wm" width="600px">

_Data Acquisition Arduino API = API Arduino para Aquisição de Dados_

<hr>

# Como usar

1. Preparando o Arduino e o sensor TRC5000:

    - Primeiro, monte o sensor TRC5000 no Arduino de acordo com as instruções seguintes.

    <img src="https://www.arduinoecia.com.br/wp-content/uploads/2013/10/Sensor-Optico-Teste-sem-led-1024x499.jpg" width="400px">

    - Em seguida, inicialize o arquivo "CodigoTRANSCONTROLardu.ino", é necessario ter a IDE do Arduino para conseguir executar o codigo 
    
    - conecte o Arduino ao seu computador usando o cabo USB apropriado.

    - Certifique-se de que o código do Arduino esteja carregado e funcionando corretamente. 

2. Clone este repositório em sua máquina.

3. Acesse o arquivo **main.js** e parametrize:

- Gostaria de efetuar a inserção dos dados capturados no Banco de Dados? **Linha 15 - HABILITAR_OPERACAO_INSERIR;**

- Para configurar as credenciais do banco de dados: adicione as credenciais para inserção no banco MySQL (**Linhas 32 - 36**) e ajuste seu INSERT para que esteja de acordo com a tabela que receberá as medidas (**Linhas 84 e 85**).

4. Acesse o local deste repositório no terminal (GitBash ou VSCode) e execute os comandos abaixo:

```
npm i
``` 
_O comando acima irá instalar as bibliotecas necessárias para o funcionamento da API. As bibliotecas a serem instaladas estão listadas no arquivo **package.json** então é muito importante que este não seja alterado. Será criada uma nova pasta/diretório chamado **node_modules** quando o comando for finalizado, que é onde as bibliotecas estão localizadas. Não altere a pasta/diretório._

```
npm start
``` 

_O comando acima irá iniciar sua API e efetuar os comandos de acordo com a sua parametrização feita nos passos anteriores._

5. Para "ver" sua API funcionando você pode visualizar os gráficos das capturas sendo exibidos no seu navegador pelo caminho **http://localhost:3300** ou efetuando SELECT no seu Banco de Dados, caso tenha optado por inseri-los.

6. Caso queira parar a API, tecle **CTRL+C** no terminal em que a API está rodando.
