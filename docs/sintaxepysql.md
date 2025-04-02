
### Sintaxe SQL X Sintaxe Pandas

> As duas instruções abaixo retornam o mesmo resultado:
#### Sintaxe SQL
```
python

# Sintaxe SQL

query5 = """SELECT Nome_Produto, AVG(Unidades_Vendidas)
            FROM tb_vendas_dsa
            WHERE Valor_Unitario > 199
            GROUP BY Nome_Produto
            HAVING AVG(Unidades_Vendidas) > 10"""
```

Observando essa sintaxe:
        
**PROS:** 

- Com essa mesma sintaxe, podemos utilizar em QUALQUER SGBD! (MYSql, Oracle, Microsoft SQL SERVER, DB2, SQLite, entre outros), ou seja, aprendemos uma vez e podemos aplicar em qualquer SGBD.
- Linguagem mais simples e mais clara, não sendo tão necessário conhecimento de programação prévio.


**CONTRAS:**

- Menos flexível em termos de programação, ficando restrito à apenas comandos SQL.
- Por ser necessário estar conectado à um banco de dados, a performance é afetada em questões de conexão de rede, em larga escala, isso tem um impacto significativo.

<br><br>

#### Sintaxe Pandas
```
python

# Sintaxe Pandas

df[df['Valor_Unitario'] > 199].groupby('Nome_Produto') \
    .filter(lambda x: x['Unidades_Vendidas'].mean() > 10) \
    .groupby('Nome_Produto')['Unidades_Vendidas'].mean()
```



    out:

    Nome_Produto
    Produto_17    14.0
    Produto_39    16.0
    Name: Unidades_Vendidas, dtype: float64



Observando essa sintaxe:
**PROS:**

- Isso que fazemos com pandas é programação, ou seja, podemos aplicar esse código em um loop, podemos usar variáveis, então, em termos de flexibilidade de programação, o pandas é mais dinâmico.
- Melhor performance, pois os dados já estarão no ambiente com o pandas!

**CONTRAS:** 

- A sintaxe do Pandas, é exclusivamente e somente, do pandas! Temos que utilizar a linguagem python, transformar em um DF do pandas para utilizar ela.
- Linguagem mais complexa exigindo um certo conhecimento de programação.

<br><br>

> **CONCLUSÃO**:

**NÃO EXISTE FERRAMENTA PERFEITA!** É nosso dever analisar e ver qual é a melhor ferramenta para cada caso em específico, **TUDO DEPENDE!!**
