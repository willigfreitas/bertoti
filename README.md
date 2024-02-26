Engenharia de software

Em relação a outras engenharias existe um controle rígido em relação a processos, padrões, a engenharia de software busca a melhor alternativa para a tomada de decisão, levando em conta os trade-offs, se o melhor sistema é monolítico ou uma arquitetura de microserviços. Uma das perguntas relevantes quando se desenvolve o software é pensar sobre sua possível vida útil. Enxergar sobre falhas a longo prazo, entre outras questões, relacionado a isso temos o conceito de sustentabilidade do software. Deve-se pensar em quais possíveis melhorias podem ser implementadas no software de acordo com o escopo, se esse programa visa algo a longo prazo ou curto prazo. 
Avaliando parte do conteúdo do livro quando abordado a respeito de trade-offs e custos (https://abseil.io/resources/swe-book/html/ch01.html#tradeoffs_and_costs), realizar boas decisões na engenharia é pesar todas as entradas disponíveis e tomar decisões que existem as informações dos tradeoffs. Às vezes, essas  decisões são baseadas no instinto ou nas melhores práticas, mas apenas depois de esgotar os métodos que tentam medir ou estimar a alocação de custos. 



- Citar 3 exemplos de trade-offs (em software) e explicá-los conforme comentários que fizemos na sexta.

- Pensando em Python e Java temos as seguintes conclusões em relação a trade-offs:

- Java - WORA -Write once run anywhere - diferente de várias outras linguagens a praticidade de você fazer um código único e cada sistema operacional irá entender. Isso é possível porque em JAVA é utilizada a JVM. Quando se escreve um código em Java o código-fonte é compilado para um formato intermediário chamado bytecode. Esse bytecode é então executado pela JVM, que está disponível para várias plataformas. No entanto várias pessoas acham que desenvolver em JAVA é mais complicado que em outras linguagens, tais como Python, pois os códigos podem envolver um pouco mais de complexidade. Um exemplo é você pedir para "printar" um resultado de um "hello world" em Python e outro em Java. Daí se nota a grande diferença.
- Python - Facilidade de codificação, vários comandos são muito simples por sua legibilidade e facilidade de se desenvolver rápidamente o código. Entretanto, essa facilidade pode resultar em um desempenho inferior em relação a outras linguagens quanto outras linguagens, tais como C++ ou Rust.
