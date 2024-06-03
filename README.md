**1. Comentários do livro SWE at Google**
------------


Em relação a outras engenharias existe um controle rígido em relação a processos, padrões, a engenharia de software busca a melhor alternativa para a tomada de decisão, levando em conta os trade-offs, se o melhor sistema é monolítico ou uma arquitetura de microserviços. Uma das perguntas relevantes quando se desenvolve o software é pensar sobre sua possível vida útil. Enxergar sobre falhas a longo prazo, entre outras questões, relacionado a isso temos o conceito de sustentabilidade do software. Deve-se pensar em quais possíveis melhorias podem ser implementadas no software de acordo com o escopo, se esse programa visa algo a longo prazo ou curto prazo. 
Avaliando parte do conteúdo do livro quando abordado a respeito de trade-offs e custos (https://abseil.io/resources/swe-book/html/ch01.html#tradeoffs_and_costs), realizar boas decisões na engenharia é pesar todas as entradas disponíveis e tomar decisões que existem as informações dos tradeoffs. Às vezes, essas  decisões são baseadas no instinto ou nas melhores práticas, mas apenas depois de esgotar os métodos que tentam medir ou estimar a alocação de custos. 



**2. Citar 3 exemplos de trade-offs (em software) e explicá-los conforme comentários que fizemos na sexta(discutir em relação a requisitos-não funcionais).**
------------

- Pensando em Python e Java temos as seguintes conclusões em relação a trade-offs:

- Java - WORA -Write once run anywhere - diferente de várias outras linguagens a praticidade de você fazer um código único e cada sistema operacional irá entender. Isso é possível porque em JAVA é utilizada a JVM. Quando se escreve um código em Java o código-fonte é compilado para um formato intermediário chamado bytecode. Esse bytecode é então executado pela JVM, que está disponível para várias plataformas. Apesar da sua portabilidade, por conta de mais camadas de abstrações necessárias para essas funções ele apresenta um desempenho ligeiramente inferior em relação a C++ e a Rust.
Embora a alocação automática de memória e o gerenciamento de lixo sejam vantagens em termos de desenvolvimento e segurança, eles podem resultar em um consumo de memória maior do que o desejado em sistemas com recursos limitados. Isso pode ser um trade-off significativo em aplicativos de alto desempenho ou em sistemas embarcados com restrições de memória.
- No entanto várias pessoas acham que desenvolver em JAVA é mais complicado que em outras linguagens, tais como Python, pois os códigos podem envolver um pouco mais de complexidade. Um exemplo é você pedir para "printar" um resultado de um "hello world" em Python e outro em Java. Daí se nota a grande diferença.
- Python - Facilidade de codificação, vários comandos são muito simples por sua legibilidade e facilidade de se desenvolver rápidamente o código. Entretanto, essa facilidade pode resultar em um desempenho inferior em relação a outras linguagens tais como C++ ou Rust. Python também oferece multiplos paradigmas de programação, programação orientada a objetos, programação funcional e programação procedural. Essa flexibilidade pode levar a códigos menos estruturados, e mais difíceis de manter em códigos grandes. Python é conhecido por sua simplicidade e legibilidade, o que facilita o desenvolvimento rápido de código. No entanto, essa simplicidade pode resultar em desempenho inferior em comparação com linguagens compiladas, como C++ ou Rust. O desenvolvedor precisa equilibrar a conveniência de escrever código rapidamente com a necessidade de desempenho otimizado.

**Atividade 3**
 --
Para cada arquitetura, escolha 2 requisitos não funcionais (um bom e outro ruim) e explique escolhendo um sistema para ser desenvolvido seguindo essa arquitetura.
--

Dentre as vantagens do sistema da **ARQUITETURA DE MICROSERVIÇOS** está projetar um aplicativo como uma coleção de serviços pequenos, independentes e altamente especializados.
Pensando em alguns exemplos podemos destacar a Uber:


- Um requisito não funcional interessante é a segurança. garantindo que os dados dos usuários e transações sejam protegidos adequadamente contra acesso não autorizado e manipulação. Isso incluiria a implementação de medidas de autenticação, criptografia e conformidade com regulamentações de privacidade de dados, como o GDPR.
- Um requisito não funcional ruim seria uma dependência excessiva da conectividade de rede para a operação do aplicativo Uber. Se o aplicativo exigir uma conexão de rede muito estável e rápida para funcionar corretamente, isso pode limitar sua utilidade em áreas com cobertura de rede deficiente ou durante interrupções na conectividade, prejudicando a experiência do usuário.

- Outro exemplo é a  Netflix:

- Bom Requisito Não Funcional: Escalabilidade

O bom requisito não funcional para a Netflix seria a escalabilidade, garantindo que o serviço seja capaz de lidar com picos de tráfego, como aqueles que ocorrem durante lançamentos de séries populares ou eventos especiais, sem queda na qualidade ou interrupções para os usuários. Isso é essencial para garantir uma experiência de streaming suave e consistente para milhões de usuários em todo o mundo.
Requisito Não Funcional Ruim: Tempo de Resposta

Um requisito não funcional ruim seria uma meta de tempo de resposta muito rígida para todas as solicitações de streaming. Se a Netflix definir um tempo de resposta extremamente baixo como um requisito inflexível, isso pode levar a decisões arquitetônicas que comprometam a escalabilidade ou a disponibilidade do sistema em favor de tempos de resposta mais rápidos.

Dentre as vantagens do sistema da ARQUITETURA ORIENTADA A EVENTOS é uma abordagem em que os componentes do sistema se comunicam por meio da geração, detecção e resposta a eventos.
Seguem alguns exemplos de sistemas: 


Internet das Coisas (IoT):

Bom Requisito Não Funcional: Escalabilidade

Um bom requisito não funcional para sistemas IoT seria a escalabilidade, garantindo que o sistema seja capaz de lidar com um grande número de dispositivos conectados e volumes crescentes de dados gerados por eles. Isso é essencial para garantir que o sistema possa suportar um aumento na adoção de dispositivos IoT sem comprometer o desempenho ou a disponibilidade.
Requisito Não Funcional Ruim: Latência de Rede

Um requisito não funcional ruim seria uma meta de latência de rede extremamente baixa para todas as comunicações entre dispositivos IoT e o backend. Se o sistema IoT definir uma meta de latência muito baixa como um requisito inflexível, isso pode limitar a escolha de tecnologias de comunicação, tornar o sistema mais complexo e caro de implementar e prejudicar a eficiência energética dos dispositivos.

**Aplicações de Monitoramento e Análise em Tempo Real**:

Bom Requisito Não Funcional: Confiabilidade

Um bom requisito não funcional para aplicações de monitoramento e análise em tempo real seria a confiabilidade, garantindo que o sistema seja altamente disponível e capaz de processar e responder a eventos críticos de forma consistente e precisa. Isso é fundamental para garantir que o sistema possa detectar e responder a problemas imediatamente, minimizando o tempo de inatividade e maximizando a eficácia do monitoramento.

Requisito Não Funcional Ruim: Custo de Processamento

Um requisito não funcional ruim seria uma restrição de custo de processamento extremamente baixa para análise em tempo real. Se o sistema de monitoramento definir um limite muito baixo para os custos de processamento como um requisito inflexível, isso pode limitar a capacidade do sistema de processar e analisar dados de forma eficiente, resultando em análises imprecisas ou incompletas e comprometendo a eficácia do monitoramento.

**A arquitetura baseada em serviços (Service-Based Architecture)** é uma abordagem na qual um sistema é dividido em serviços independentes e interconectados, cada um executando uma função específica e sendo acessado por meio de interfaces bem definidas. 

Amazon Web Services (AWS):

Bom Requisito Não Funcional: Escalabilidade

Um bom requisito não funcional para a AWS seria a escalabilidade, garantindo que todos os serviços da AWS sejam altamente escaláveis para atender às demandas crescentes dos usuários. Isso inclui garantir que os serviços possam escalar horizontalmente de forma automática e eficiente para lidar com picos de tráfego, garantindo um alto nível de desempenho e disponibilidade para os clientes da AWS.

Requisito Não Funcional Ruim: Disponibilidade Limitada

Um requisito não funcional ruim seria uma disponibilidade limitada para qualquer serviço da AWS. Se um serviço tiver uma disponibilidade limitada, isso pode causar interrupções no serviço para os clientes, afetando negativamente a confiança no serviço e prejudicando a reputação da AWS como um provedor de serviços em nuvem confiável e de alta disponibilidade.
Salesforce:

Bom Requisito Não Funcional: Segurança

Um bom requisito não funcional para Salesforce seria a segurança, garantindo que todos os dados armazenados e processados pelos serviços da Salesforce sejam protegidos adequadamente contra acesso não autorizado e violações de segurança. Isso inclui garantir que todos os serviços da Salesforce sigam as melhores práticas de segurança, como criptografia de dados, controle de acesso e monitoramento de atividades suspeitas.
Requisito Não Funcional Ruim: Desempenho Insatisfatório

Um requisito não funcional ruim seria um desempenho insatisfatório para qualquer serviço da Salesforce. Se um serviço da Salesforce tiver um desempenho insatisfatório, isso pode levar a tempos de resposta lentos para os usuários, afetando negativamente a experiência do usuário e a eficiência operacional das organizações que dependem dos serviços da Salesforce para suas operações de negócios.


**A arquitetura de microkernel** é um estilo arquitetural que separa o núcleo mínimo (microkernel) das funcionalidades adicionais do sistema, permitindo uma maior modularidade e flexibilidade.

Hypervisores (Hipervisores):

Bom Requisito Não Funcional: Isolamento de Recursos

Um bom requisito não funcional para hipervisores seria o isolamento eficaz de recursos entre as máquinas virtuais. Isso garante que cada máquina virtual tenha seus próprios recursos de CPU, memória e armazenamento isolados dos outros, proporcionando segurança e estabilidade para os sistemas hospedados. Um hipervisor com um alto nível de isolamento de recursos oferece uma garantia sólida de que as cargas de trabalho de uma máquina virtual não interferirão nas outras.

Requisito Não Funcional Ruim: Sobrecarga de Desempenho

Um requisito não funcional ruim seria uma sobrecarga excessiva de desempenho causada pela **arquitetura de microkernel** do hipervisor. Embora a arquitetura de microkernel ofereça benefícios em termos de modularidade e flexibilidade, ela também pode introduzir uma sobrecarga adicional devido à necessidade de comunicação entre os componentes do microkernel. Se a sobrecarga for muito alta, isso pode afetar negativamente o desempenho das máquinas virtuais hospedadas, reduzindo a eficiência da virtualização.
QNX:

Bom Requisito Não Funcional: Tempo de Resposta em Tempo Real

Um bom requisito não funcional para o QNX seria um tempo de resposta previsível e consistente em tempo real para eventos críticos. A natureza em tempo real do QNX o torna adequado para sistemas onde a resposta imediata a eventos é essencial, como em sistemas de controle de automóveis, dispositivos médicos e sistemas de automação industrial. Um requisito de tempo de resposta em tempo real bem atendido garante que o QNX possa lidar com eventos críticos de forma rápida e confiável.
Requisito Não Funcional Ruim: Complexidade de Desenvolvimento

Um requisito não funcional ruim seria uma complexidade de desenvolvimento excessiva causada pela **arquitetura de microkernel** do QNX. Embora a arquitetura de microkernel ofereça benefícios em termos de modularidade e manutenibilidade, ela também pode introduzir uma complexidade adicional no desenvolvimento de aplicativos devido à necessidade de comunicação entre os diferentes componentes do microkernel. Se a complexidade de desenvolvimento for muito alta, isso pode aumentar o custo e o tempo de desenvolvimento de aplicativos para o QNX.

**A arquitetura de pipeline** é uma abordagem em que as tarefas de processamento são divididas em etapas discretas, e cada etapa é realizada de forma sequencial, com os resultados sendo passados de uma etapa para a próxima.

Compiladores:

Bom Requisito Não Funcional: Eficiência de Processamento

Um bom requisito não funcional para compiladores é a eficiência de processamento. Isso envolve garantir que cada etapa do pipeline do compilador seja otimizada para processar o código fonte de forma rápida e eficiente. Um compilador eficiente pode reduzir significativamente o tempo necessário para compilar grandes projetos de software, melhorando a produtividade dos desenvolvedores.

Requisito Não Funcional Ruim: Precisão dos Resultados

Um requisito não funcional ruim seria uma precisão insatisfatória dos resultados. Se o compilador não garantir a precisão das transformações realizadas em cada etapa do pipeline, isso pode levar a erros de compilação ou comportamento inesperado do programa final. A precisão dos resultados é essencial para garantir a confiabilidade e a qualidade do código compilado.

**A arquitetura em camadas (Layered Architecture)** é um estilo arquitetural em que o sistema é dividido em camadas ou níveis distintos, onde cada camada é responsável por um conjunto específico de funcionalidades.

Redes de Computadores:

Bom Requisito Não Funcional: Latência de Processamento

Um bom requisito não funcional para redes de computadores é a latência de processamento. Isso envolve garantir que os pacotes de dados sejam processados rapidamente em cada etapa do pipeline de roteamento, com o mínimo de atraso possível. Uma baixa latência de processamento é crucial para garantir tempos de resposta rápidos e uma comunicação eficiente na rede.

Requisito Não Funcional Ruim: Perda de Pacotes

Um requisito não funcional ruim seria uma alta taxa de perda de pacotes. Se os sistemas de rede não garantirem a integridade dos pacotes de dados em cada etapa do pipeline de roteamento, isso pode resultar em pacotes perdidos ou corrompidos, afetando a confiabilidade e a qualidade da comunicação na rede. A perda de pacotes pode levar a uma experiência de usuário ruim e impactar negativamente a disponibilidade dos serviços de rede.

Aplicações Web Tradicionais:

Bom Requisito Não Funcional: Segurança dos Dados

Um bom requisito não funcional para aplicações web tradicionais é a segurança dos dados. Ao adotar uma **arquitetura em camadas**, é fundamental garantir que os dados sensíveis dos usuários estejam protegidos em todas as camadas, desde a camada de apresentação até a camada de armazenamento de dados. Isso pode incluir criptografia de dados, autenticação robusta, autorização adequada e práticas de segurança recomendadas em todas as partes da aplicação.

Requisito Não Funcional Ruim: Desempenho Lento da Interface do Usuário

Um requisito não funcional ruim seria um desempenho lento da interface do usuário. Se **a arquitetura em camadas** não for adequadamente otimizada, isso pode levar a atrasos perceptíveis na renderização e na resposta da interface do usuário, prejudicando a experiência do usuário. Isso pode ser causado por uma má distribuição de tarefas entre as camadas, gargalos de comunicação ou operações de processamento excessivamente complexas na camada de apresentação.

Aplicações Móveis:

Bom Requisito Não Funcional: Consumo Eficiente de Energia

Um bom requisito não funcional para aplicações móveis é o consumo eficiente de energia. Ao seguir **uma arquitetura em camadas**, é importante projetar a aplicação de forma a minimizar o consumo de energia, especialmente em dispositivos móveis com recursos limitados de bateria. Isso pode envolver otimizações de código, gerenciamento eficiente de recursos e minimização de operações em segundo plano que possam drenar a bateria do dispositivo.

Requisito Não Funcional Ruim: Latência Excessiva na Comunicação com o Servidor

Um requisito não funcional ruim seria uma latência excessiva na comunicação com o servidor. Se a arquitetura em camadas não for eficientemente projetada e implementada, isso pode resultar em tempos de resposta lentos para solicitações de dados do servidor, causando atrasos perceptíveis e frustração para os usuários. Isso pode ser causado por problemas de rede, sobrecarga de processamento no servidor ou ineficiências na comunicação entre as camadas da aplicação móvel.


**4. Definição da arquitetura (à partir de  sistema escolhido)**
--
**Netflix**

Conhecida por sua arquitetura de microserviços. Cada função do sistema, como recomendações, reprodução de vídeo, gerenciamento de contas, entre outros, é tratada por microserviços separados. Isso permite que a Netflix se adapte rapidamente às mudanças no tráfego de usuários e ofereça uma experiência personalizada.

**5. Classes uml**
--
![UML DEF](https://github.com/willigfreitas/bertoti/assets/48508462/2c8f85f9-eb68-4aa9-bffc-e62febffc57c)


**6. código java**
--

```
//Netflix.java

import java.util.LinkedList;
import java.util.List;

public class Netflix {
    // Declaração das listas de filmes e usuários
    private List<Filme> filmes = new LinkedList<>();
    private List<Usuario> usuarios = new LinkedList<>();

    // Método para cadastrar um novo filme
    public void cadastrarFilme(Filme filme) {
        filmes.add(filme);
    }

    // Método para buscar filmes por título
    public List<Filme> buscarFilmePorTitulo(String nome) {
        List<Filme> filmesEncontrados = new LinkedList<>();
        for (Filme filme : filmes) {
            if (filme.getNome().equals(nome)) {
                filmesEncontrados.add(filme);
            }
        }
        return filmesEncontrados;
    }

    // Método para buscar filmes por gênero
    public List<Filme> buscarFilmePorGenero(String genero) {
        List<Filme> filmesEncontrados = new LinkedList<>();
        for (Filme filme : filmes) {
            if (filme.getGenero().equals(genero)) {
                filmesEncontrados.add(filme);
            }
        }
        return filmesEncontrados;
    }

    // Método para cadastrar um novo usuário
    public void cadastrarUsuario(Usuario usuario) {
        usuarios.add(usuario);
    }

    // Método para fazer login de um usuário
    public boolean login(Usuario usuario) {
        for (Usuario u : usuarios) {
            if (u.getNome().equals(usuario.getNome()) && u.getSenha().equals(usuario.getSenha())) {
                return true;
            }
        }
        return false;
    }

    // Getters e setters para filmes e usuários
    public List<Filme> getFilmes() {
        return filmes;
    }

    public void setFilmes(List<Filme> filmes) {
        this.filmes = filmes;
    }

    public List<Usuario> getUsuarios() {
        return usuarios;
    }

    public void setUsuarios(List<Usuario> usuarios) {
        this.usuarios = usuarios;
    }
}

```

```
//Filme.java

public class Filme {
    private String titulo;
    private String genero;

    // Construtor para inicializar titulo e genero
    public Filme(String titulo, String genero) {
        this.titulo = titulo;
        this.genero = genero;
    }

    // Métodos getters e setters para titulo e genero
    public String getTitulo() {
        return titulo;
    }

    public void setTitulo(String titulo) {
        this.titulo = titulo;
    }

    public String getGenero() {
        return genero;
    }

    public void setGenero(String genero) {
        this.genero = genero;
    }

    // Método para obter detalhes do filme (aqui retornamos apenas o título)
    public String getDetalhesFilme() {
        return "Título: " + titulo + ", Gênero: " + genero;
    }

    // Método para definir detalhes do filme (aqui apenas definimos o título e o gênero)
    public void setDetalhesFilme(String titulo, String genero) {
        this.titulo = titulo;
        this.genero = genero;
    }

    // Método para obter o título do filme (duplicado)
    // Este método pode ser removido se não houver necessidade específica para ele
    public String getNome() {
        return titulo;
    }

    // Método para definir o título do filme (duplicado)
    // Este método pode ser removido se não houver necessidade específica para ele
    public void setNome(String titulo) {
        this.titulo = titulo;
    }
}
```


```
//Usuario.java

import java.util.LinkedList;
import java.util.List;

public class Usuario {
    private String nome;
    private String senha;
    private List<Filme> filmes = new LinkedList<>();

    // Construtor para inicializar nome e senha
    public Usuario(String nome, String senha) {
        this.nome = nome;
        this.senha = senha;
    }

    // Método para adicionar um novo filme
    public void cadastrarFilme(Filme filme) {
        filmes.add(filme);
    }

    // Método para remover um filme
    public void removerFilme(Filme filme) {
        filmes.remove(filme);
    }

    // Método para assistir a um filme
    public void assistirFilme(Filme filme) {
        // Lógica para assistir ao filme
        System.out.println("Assistindo ao filme: " + filme.getTitulo());
    }

    // Método para definir a lista de filmes
    public void setFilmes(List<Filme> filmes) {
        this.filmes = filmes;
    }

    // Método para obter a lista de filmes
    public List<Filme> getFilmes() {
        return filmes;
    }

    // Getters e setters para nome e senha
    public String getNome() {
        return nome;
    }

    public void setNome(String nome) {
        this.nome = nome;
    }

    public String getSenha() {
        return senha;
    }

    public void setSenha(String senha) {
        this.senha = senha;
    }
}
```

**7. TESTES**

```
//FilmeTest.java

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class FilmeTest {

    @Test
    public void testFilme() {
        Filme filme = new Filme("Matrix", "Action");
        assertEquals("Matrix", filme.getTitulo());
        assertEquals("Action", filme.getGenero());

        filme.setTitulo("Inception");
        filme.setGenero("Sci-Fi");
        assertEquals("Inception", filme.getTitulo());
        assertEquals("Sci-Fi", filme.getGenero());

        String detalhes = filme.getDetalhesFilme();
        assertEquals("Título: Inception, Gênero: Sci-Fi", detalhes);
    }
}
```

```
//NetflixTest.java

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

import java.util.List;

public class NetflixTest {

    @Test
    public void testCadastrarFilme() {
        Netflix netflix = new Netflix();
        Filme filme = new Filme("Matrix", "Ficção Científica");
        netflix.cadastrarFilme(filme);
        
        List<Filme> filmes = netflix.getFilmes();
        assertEquals(1, filmes.size());
        assertEquals("Matrix", filmes.get(0).getNome());
    }

    @Test
    public void testBuscarFilmePorTitulo() {
        Netflix netflix = new Netflix();
        Filme filme1 = new Filme("Matrix", "Ficção Científica");
        Filme filme2 = new Filme("Matrix Reloaded", "Ficção Científica");
        netflix.cadastrarFilme(filme1);
        netflix.cadastrarFilme(filme2);
        
        List<Filme> filmes = netflix.buscarFilmePorTitulo("Matrix");
        assertEquals(1, filmes.size());
        assertEquals("Matrix", filmes.get(0).getNome());
    }

    @Test
    public void testBuscarFilmePorGenero() {
        Netflix netflix = new Netflix();
        Filme filme1 = new Filme("Matrix", "Ficção Científica");
        Filme filme2 = new Filme("Inception", "Ficção Científica");
        Filme filme3 = new Filme("Titanic", "Romance");
        netflix.cadastrarFilme(filme1);
        netflix.cadastrarFilme(filme2);
        netflix.cadastrarFilme(filme3);
        
        List<Filme> filmes = netflix.buscarFilmePorGenero("Ficção Científica");
        assertEquals(2, filmes.size());
    }

    @Test
    public void testCadastrarUsuario() {
        Netflix netflix = new Netflix();
        Usuario usuario = new Usuario("john", "1234");
        netflix.cadastrarUsuario(usuario);
        
        List<Usuario> usuarios = netflix.getUsuarios();
        assertEquals(1, usuarios.size());
        assertEquals("john", usuarios.get(0).getNome());
    }

    @Test
    public void testLogin() {
        Netflix netflix = new Netflix();
        Usuario usuario = new Usuario("john", "1234");
        netflix.cadastrarUsuario(usuario);
        
        assertTrue(netflix.login(new Usuario("john", "1234")));
        assertFalse(netflix.login(new Usuario("john", "wrongpassword")));
    }
}
```

```
//UsuarioTest.java

import org.junit.jupiter.api.Test;
import static org.junit.jupiter.api.Assertions.*;

public class UsuarioTest {

    @Test
    public void testUsuario() {
        Usuario usuario = new Usuario("john_doe", "password123");

        assertEquals("john_doe", usuario.getNome());
        assertEquals("password123", usuario.getSenha());

        Filme filme1 = new Filme("Matrix", "Action");
        Filme filme2 = new Filme("Inception", "Sci-Fi");

        usuario.cadastrarFilme(filme1);
        usuario.cadastrarFilme(filme2);

        assertTrue(usuario.getFilmes().contains(filme1));
        assertTrue(usuario.getFilmes().contains(filme2));

        usuario.removerFilme(filme1);
        assertFalse(usuario.getFilmes().contains(filme1));

        usuario.assistirFilme(filme2);  // Verifique se o filme é impresso corretamente no console
    }
}
```

--
