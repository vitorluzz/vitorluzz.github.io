

### **GROUP BY**

Essa, é uma das cláusulas mais complicadas da linguagem. Bom, vamos supor que queremos a média, o valor mínimo, o valor máximo, a soma e a contagem de uma tabela que contém as vendas dos produtos, observe essa Query:

**FORMA ERRADA! ❌**
```SQL title='SQL'
SELECT Produto, 
    MIN(Valor_Venda), 
    MAX(Valor_Venda), 
    AVG(Valor_Venda), 
    SUM(Valor_Venda), 
    COUNT(Valor_Venda) 
FROM Vendas;
```

> Por mais que colocamos a coluna Produtos em primeiro, isso não irá funcionar! Estamos fazendo isso para apenas 1 Produto e não fazendo isso em específico para cada produto.

**FORMA CORRETA! ✅**

```SQL title='SQL'
SELECT Produto, 
    MIN(Valor_Venda) AS "Valor Mínimo", 
    MAX(Valor_Venda) AS "Valor Máximo", 
    AVG(Valor_Venda) AS "Média", 
    SUM(Valor_Venda) AS "Total", 
    COUNT(Valor_Venda)  AS "Contagem"
FROM Vendas
GROUP BY Produto;
```

> Agora sim está correto! O Group By serve exatamente pra isso, para podermos executar essas funções para CADA PRODUTO.
