# Cypress 4 E2E

A principio o objetivo desse repo é discorrer sobre o uso da ferramenta Cypress para a realização dos testes de integração.

Demonstrarei como essa ferramenta pode ser utilizada para testes tanto no back-end quanto no front-end com uma performance tão boa quanto, quiçá melhor, que as ferramentas utilizadas hoje, mas não apenas isso, como também evidenciar o quanto o uso dessa tecnologia pode facilitar a compreensão do projeto de testes e em paralelo apoiar o workflow no que diz respeito a Continuos Integration (CI), Automação de testes, Integração com Pipeline, etc.

Inicialmente irei realizar os teste utilizando um ambiente totalmente mockado para dessa forma não correr riscos em relação a dados sensíveis.  [Usar fakeJSONAPI ao invés do projeto real !]

A princípio é importante demonstrar o quanto essa ferramenta é versátil em todos os cenários, portanto, a abordagem será a seguinte:

## Iniciando os testes

Para iniciar o procedimento de testes é importante notar que iremos utilizar a aplicação json-server para mockar uma base de dados fake baseada no arquivo `utils/data/db.json`
Para rodar o server basta utilizar o comando em ambiente de terminal: 

```bash
npm run fake-api
```

O servidor portanto irá rodar em `localhost:3333` ou na porta especificada no arquivo package.json

## Ferramentas utilizadas

### Json-Server


### Cypress
Obviamente irei utilizar o Cypress para realizar e orquestrar nossos cases de teste.
Essa ferramenta é principalmente utilizada para testes frontend, contudo, por ser versátil ele permite que sejam testados cenários de teste envolvendo também o cenário backend.

### Cucumber
Irei utilizar, como é de praxe o BDD como estruturador dos cenários de teste. Optei pelo cucumber que já é a ferramenta que mais utilizamos para esses casos de teste e, para além disso permite relativa fácil integração coim o cypress e a estrutura de diretórios dessa aplicação.

### Express
O express será utilizado para realizar requests ao back end de forma que conseguimos verificar ainda melhor o corpo da response.