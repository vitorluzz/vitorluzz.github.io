Transformer (Transformador), é basicamente uma arquitetura de rede neural que revoluciou o campo de processamento de linguagem natural (PLN) e outras áreas em Deep Learning.

Abaixo o diagrama da arquitetura de transformadores:

<img src='../../../../assets/arquiteturatransformer.png' style='margin-left: 10vw;width: 30vw;'>

O conceito central do transformer é o mecanismo de atenção, especificamente a atenção automática (self-attention). Este mecanismo permite que o modelo examine e considere diferentes partes de uma sequência de entrada (como palavras em uma frase) simultaneamente, ponderando a importância de cada parte com relação às outras.

Podemos comparar isso com as redes neurais recorrentes, que processam sequências de forma sequencial, cada etapa por vez, o que limita a capacidade de capturar dependências de longo alcance.

O transformer é composto por duas partes principais:

**Codificador (Encoder):** Recebe a sequência de entrada e gera uma representação interna dessa sequência, capturando as relações entre os diferentes elementos de entrada

**Decodificador (Decoder):** Usa essa representação interna para gerar uma sequência de saída, como uma tradução ou um resumo.


A inovação mais significativa do Transformer é a utilização de atenção multi-cabeças (multi-heads attention), que permite ao modelo focar em diferentes partes da sequência simultaneamente, capturando múltiplos aspectos das dependências entre palavras.

Os transformadores são altamente paralelízáveis, o que os torna mais eficientes em termos de treinamento em comparação com RNNs e LSTMs (Long Short-Term Mentory)