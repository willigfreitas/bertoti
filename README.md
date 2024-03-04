Engenharia de software

Em relação a outras engenharias existe um controle rígido em relação a processos, padrões, a engenharia de software busca a melhor alternativa para a tomada de decisão, levando em conta os trade-offs, se o melhor sistema é monolítico ou uma arquitetura de microserviços. Uma das perguntas relevantes quando se desenvolve o software é pensar sobre sua possível vida útil. Enxergar sobre falhas a longo prazo, entre outras questões, relacionado a isso temos o conceito de sustentabilidade do software. Deve-se pensar em quais possíveis melhorias podem ser implementadas no software de acordo com o escopo, se esse programa visa algo a longo prazo ou curto prazo. 
Avaliando parte do conteúdo do livro quando abordado a respeito de trade-offs e custos (https://abseil.io/resources/swe-book/html/ch01.html#tradeoffs_and_costs), realizar boas decisões na engenharia é pesar todas as entradas disponíveis e tomar decisões que existem as informações dos tradeoffs. Às vezes, essas  decisões são baseadas no instinto ou nas melhores práticas, mas apenas depois de esgotar os métodos que tentam medir ou estimar a alocação de custos. 



- Citar 3 exemplos de trade-offs (em software) e explicá-los conforme comentários que fizemos na sexta(discutir em relação a requisitos-não funcionais).

-Pensando em Python e Java temos as seguintes conclusões em relação a trade-offs:

- Java - WORA -Write once run anywhere - diferente de várias outras linguagens a praticidade de você fazer um código único e cada sistema operacional irá entender. Isso é possível porque em JAVA é utilizada a JVM. Quando se escreve um código em Java o código-fonte é compilado para um formato intermediário chamado bytecode. Esse bytecode é então executado pela JVM, que está disponível para várias plataformas. Apesar da sua portabilidade, por conta de mais camadas de abstrações necessárias para essas funções ele apresenta um desempenho ligeiramente inferior em relação a C++ e a Rust.
Embora a alocação automática de memória e o gerenciamento de lixo sejam vantagens em termos de desenvolvimento e segurança, eles podem resultar em um consumo de memória maior do que o desejado em sistemas com recursos limitados. Isso pode ser um trade-off significativo em aplicativos de alto desempenho ou em sistemas embarcados com restrições de memória.
- No entanto várias pessoas acham que desenvolver em JAVA é mais complicado que em outras linguagens, tais como Python, pois os códigos podem envolver um pouco mais de complexidade. Um exemplo é você pedir para "printar" um resultado de um "hello world" em Python e outro em Java. Daí se nota a grande diferença.
- Python - Facilidade de codificação, vários comandos são muito simples por sua legibilidade e facilidade de se desenvolver rápidamente o código. Entretanto, essa facilidade pode resultar em um desempenho inferior em relação a outras linguagens tais como C++ ou Rust. Python também oferece multiplos paradigmas de programação, programação orientada a objetos, programação funcional e programação procedural. Essa flexibilidade pode levar a códigos menos estruturados, e mais difíceis de manter em códigos grandes. Python é conhecido por sua simplicidade e legibilidade, o que facilita o desenvolvimento rápido de código. No entanto, essa simplicidade pode resultar em desempenho inferior em comparação com linguagens compiladas, como C++ ou Rust. O desenvolvedor precisa equilibrar a conveniência de escrever código rapidamente com a necessidade de desempenho otimizado.

Atividade 3
 
Para cada arquitetura, escolha 2 requisitos não funcionais (um bom e outro ruim) e explique escolhendo um sistema para ser desenvolvido seguindo essa arquitetura.


Dentre as vantagens do sistema da ARQUITETURA DE MICROSERVIÇOS está projetar um aplicativo como uma coleção de serviços pequenos, independentes e altamente especializados.
Pensando em alguns exemplos podemos destacar a Uber:

- Um requisito não funcional interessante é a segurança. garantindo que os dados dos usuários e transações sejam protegidos adequadamente contra acesso não autorizado e manipulação. Isso incluiria a implementação de medidas de autenticação, criptografia e conformidade com regulamentações de privacidade de dados, como o GDPR.
- Um requisito não funcional ruim seria uma dependência excessiva da conectividade de rede para a operação do aplicativo Uber. Se o aplicativo exigir uma conexão de rede muito estável e rápida para funcionar corretamente, isso pode limitar sua utilidade em áreas com cobertura de rede deficiente ou durante interrupções na conectividade, prejudicando a experiência do usuário.

- Outro exemplo exemplo é a Netflix:

- Bom Requisito Não Funcional: Escalabilidade

O bom requisito não funcional para a Netflix seria a escalabilidade, garantindo que o serviço seja capaz de lidar com picos de tráfego, como aqueles que ocorrem durante lançamentos de séries populares ou eventos especiais, sem queda na qualidade ou interrupções para os usuários. Isso é essencial para garantir uma experiência de streaming suave e consistente para milhões de usuários em todo o mundo.
Requisito Não Funcional Ruim: Tempo de Resposta

Um requisito não funcional ruim seria uma meta de tempo de resposta muito rígida para todas as solicitações de streaming. Se a Netflix definir um tempo de resposta extremamente baixo como um requisito inflexível, isso pode levar a decisões arquitetônicas que comprometam a escalabilidade ou a disponibilidade do sistema em favor de tempos de resposta mais rápidos.

