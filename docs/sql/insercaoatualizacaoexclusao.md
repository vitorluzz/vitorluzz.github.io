

### **INSERT**

Podemos ainda inserir registros em uma tabela com o comando INSERT, por exemplo:

```SQL title='SQL'
INSERT INTO Clientes(
                        ID_Cliente,
                        Nome_Cliente,
                        Cidade,
                        Estado,
                        Pais,
                        Regiao,
                        Mercado,
                        Segmento
            )VALUES(
                        '1000',
                        'Bob',
                        'Teste',
                        'Estado',
                        'Pais',
                        'Regiao',
                        'Mercado',
                        'Segmento'
                    );
```
> Dessa forma, inserimos um novo registro na tabela.

Deixamos estruturado assim para melhor visualização, porém:

```SQL title='SQL'
INSERT INTO Clientes(ID_Cliente, Nome_Cliente, Cidade, Estado, Pais, Regiao, Mercado, Segmento)VALUES('1000', 'Bob', 'Teste', 'Estado', 'Pais', 'Regiao', 'Mercado', 'Segmento');
```

Dessa forma também irá funcionar com o mesmo resultado.

---

### **UPDATE**

O comando UPDATE pode ser usado para atualizarmos algum registro na tabela, ele segue essas sintaxe:

```SQL title='SQL'
UPDATE Cliente
    SET Nome_Cliente = 'Joãozinho'
WHERE ID_Cliente = '1000'; 
```

> Primeiro especificamos a tabela, depois setamos a coluna a ser modificada e depois colocamos o WHERE para especificar o registro a ser modificado.

**ATENÇÃO!** A cláusula Where se torna OBRIGATÓRIA para atualizar, pois, sem a cláusula ele irá **atualizar TODAS AS LINHAS** do seu database!

---

### **DELETE**

Podemos deletar um registo de uma tabela em específico, por exemplo:

```SQL title='SQL'
DELETE FROM Clientes
    Where ID_Cliente = '1000';
```

> Dessa forma, removemos todos os registros do cliente de ID 1000.

**ATENÇÃO:** **Sem** a cláusula **Where**, ele irá **apagar TODOS OS REGISTROS de sua tabela**, então ela se faz **obrigatória!**