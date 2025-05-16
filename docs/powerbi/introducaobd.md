O Power BI permite conectar-se a um banco de dados para visualizar e analisar informações. No entanto, **atenção:** ele **não substitui um Sistema de Gerenciamento de Banco de Dados (SGBD)**. Apenas por meio do SGBD é possível administrar o banco de dados, controlar acessos, realizar backups e executar outras tarefas de gerenciamento.

---

## Conectando à um banco de dados

O PowerBI nativamente oferece suporte a diversos bancos de dados, porém, precisamos de um conector (driver) para permitir a comunicação do PowerBI com outro software. Cada banco de dados irá ter um tipo de driver diferente.

Ou seja, toda vez que eu for entrar em um banco de dados, eu teria que instalar um driver específico para cada um. Mas tem uma forma de melhorar isso utilizando ODBC.

### ODBC (Open Database Connectivity)

**O que é ODBC?** 

ODBC é um padrão de conector para qualquer tipo de banco de dados, feito pela Microsoft, nos permite conectar em diversos bancos de dados, como Oracle, SQL Server, MySQL, PostgreSQL, entre outros.

Ele funciona usando drives específicos para cada SGBD, esses  drivers  são responsáveis por traduzir as chamadas de API do ODBC para comandos específicos do SGBD.

Então, para cada banco de dados, é necessário instalar o driver ODBC e configurar a conexão via seu sistema operacional.

---