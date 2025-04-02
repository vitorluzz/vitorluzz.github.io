
## **Armazenamento de Dados: Por que é importante?**

Hoje temos muitas alternativas para armazenamento de dados. Saber qual a melhor opção e ter **maestria** para construir o melhor layout de armazenamento é essencial.

A escolha do armazenamento depende de fatores como:
- Quantos sistemas irão acessar esse armazenamento?
- Em qual frequência?
- Qual o volume de dados lidos?
- Qual a lógica aplicada nesse sistema?

### **SQL vs NoSQL vs Armazenamento de Arquivos**
- **SQL**: Estruturado, ideal para dados organizados.
- **NoSQL**: Ideal para Big Data e dados não tabulares.
- **Armazenamento de Arquivos**: Para vídeos, imagens e outros formatos não relacionais.

### **Os 4Vs do Big Data**
1. **Volume**
2. **Velocidade**
3. **Variedade**
4. **Veracidade**

---

## Tipos de Armazenamento de Dados

### **Data Warehouse (DW)**
Um banco de dados para **análises eficientes** e de grande volume de dados, normalmente usado para integrar dados de várias fontes.

📌 **Quando usar?**
- Grande volume de dados
- Necessidade de consultas analíticas rápidas
- Integração de dados de várias fontes
- Alimentação de BI e relatórios

Os dados armazenados no DW **devem estar limpos e organizados**!

---

### **Data Lake (DL)**
O **Data Lake** armazena **todo tipo de dado**, estruturado ou não.  

Se não houver **governança** adequada, ele pode virar um "pântano de dados" (Data Swamp), tornando-se inutilizável.

📌 **Quando usar?**
- Armazenamento e processamento de dados brutos
- Grandes volumes de dados
- Dados estruturados e não estruturados
- Escalabilidade e centralização de dados

---

### **Data Lakehouse**
Une o melhor do **Data Warehouse** e do **Data Lake**, trazendo **flexibilidade e escalabilidade**.

📌 **Vantagens:**
- Boa escalabilidade e flexibilidade
- Melhor desempenho de consulta
- Centralização dos dados

📌 **Desvantagens:**
- Maior complexidade
- Uso intensivo de recursos
- Desafios de governança

---

### **Data Store**
É um **repositório para armazenar e gerenciar dados**, podendo ser local, em rede, distribuído ou na nuvem.  

📌 **Quando usar?**
- Armazenamento de arquivos
- Chave-valor
- Pesquisa de textos
- Fila de mensagens

---

### **Formatos de Arquivo**
- **Parquet**: Armazenamento colunar eficiente, ideal para Big Data.
- **Avro/ORC**: Alternativas eficientes para grandes volumes de dados.
- **CSV**: Simples e leve, mas sem compressão e cabeçalhos estruturados.
- **JSON**: Muito utilizado em aplicações web.

---