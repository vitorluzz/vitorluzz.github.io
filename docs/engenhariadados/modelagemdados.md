
## Modelagem de Dados  

### Dados - Definição  
Dados são valores, observações ou resultados armazenados em um sistema ou base de dados.  
Os dados por si só não têm tanto valor, mas quando convertidos em informações, tornam-se extremamente valiosos.  

***

### Modelagem de Dados - Definição  
A modelagem de dados é o processo de projetar e criar modelos e estruturas lógicas que representam como os dados serão armazenados, relacionados e utilizados.  

***

### Modelagem Relacional  
- Baseada em relações entre entidades, com tabelas e campos  
- Inclui modelos 1:1, 1:N e N:N  
- Utilizada em bancos de dados relacionais transacionais  

***

### Modelagem Dimensional  
- Utilizada em BI e DW  
- Facilita a análise multidimensional de dados  
- Construída a partir de **Fatos** (tabelas de medidas) e **Dimensões** (tabelas de contexto)  

***

### Modelagem de Data Lakes  
- Projetada para armazenar dados não estruturados  
- Flexível e menos estruturada que a modelagem relacional  

***

### Esquema em Modelagem de Dados  
- **DW e bancos transacionais:** Esquema obrigatório  
- **Data Lakes:** Não possuem esquema pré-definido, mas requerem organização  

***

### Constraints  
Regras aplicadas a um banco de dados para garantir a integridade dos dados, como:  
- Valores únicos  
- Restrições de valor nulo  
- Regras de validação  

***


### Formas Normais  
Regras para estruturar bancos de dados transacionais:  
- **1ª Forma Normal (1FN):** Todos os valores devem ser indivisíveis  
- **2ª Forma Normal (2FN):** Todos os atributos não-chave devem depender da chave primária  
- **3ª Forma Normal (3FN):** Evita dependências transitivas entre atributos  

***


### Projeto de Índices  
Os índices melhoram a performance de consultas, devendo ser bem planejados para:  
- Identificar colunas mais utilizadas  
- Escolher o tipo adequado de índice  
- Criar índices apenas em tabelas grandes  
- Monitorar e otimizar regularmente  

***


### Particionamento  
Técnica que divide grandes tabelas em partes menores, melhorando:  
- Desempenho  
- Manutenção  
- Escalabilidade  

> **"O Arquiteto de Dados planeja e projeta. O Engenheiro de Dados executa e mantém."**


***

### Granularidade  
Refere-se ao nível de detalhe dos dados armazenados. Quanto maior a granularidade, mais detalhados os dados serão.  

---
