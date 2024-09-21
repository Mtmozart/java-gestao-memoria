## 💻 Sobre o projeto

Voll.med é uma clínica médica fictícia que precisa de um aplicativo para gestão de consultas. O aplicativo deve possuir
funcionalidades que permitam o cadastro de médicos e de pacientes, e também o agendamento e cancelamento de consultas.

Enquanto um time de desenvolvimento será responsável pelo aplicativo mobile, o nosso será responsável pelo
desenvolvimento da API Rest desse projeto.

---

## ⚙️ Funcionalidades

- [x] CRUD de médicos;
- [x] CRUD de pacientes;
- [x] Agendamento de consultas;
- [x] Cancelamento de consultas;

---

## 🎨 Layout

O layout da aplicação mobile está disponível neste
link: <a href="https://www.figma.com/file/N4CgpJqsg7gjbKuDmra3EV/Voll.med">Figma</a>

---

## 📄 Documentação

A documentação das funcionalidades da aplicação pode ser acessada neste
link: <a href="https://trello.com/b/O0lGCsKb/api-voll-med">Trello</a>

---

## 🛠 Tecnologias

As seguintes tecnologias foram utilizadas no desenvolvimento da API Rest do projeto:

- **[Java 17](https://www.oracle.com/java)**
- **[Spring Boot 3](https://spring.io/projects/spring-boot)**
- **[Maven](https://maven.apache.org)**
- **[MySQL](https://www.mysql.com)**
- **[Hibernate](https://hibernate.org)**
- **[Flyway](https://flywaydb.org)**
- **[Lombok](https://projectlombok.org)**

---

## 📝 Licença

Projeto desenvolvido por [Alura](https://www.alura.com.br) e utilizado nos cursos de Spring Boot.

Instrutor: [Rodrigo Ferreira](https://cursos.alura.com.br/user/rodrigo-ferreira)

---

# Pilhas

Stack Overflow Error. Ele acontece quando a pilha de execução, que armazena as chamadas de métodos, fica cheia. Isso
geralmente ocorre quando um método chama a si mesmo repetidamente, criando um loop infinito.

Pilha java:

Um método main que chama um método que tem seus próprios métodos.

Recursão de cauda:
recursão de cauda. O último ato dessa função é chamar a si mesma, ou seja, não há mais cálculos a serem feitos depois
dessa chamada, não estamos colocando mais nada na pilha além da chamada de fatorialAux para n-1.

Outros pontos, todo objeto novo é criado na heap o que vemos quando chamamos métodos sem toString, vemos somente a
referência.

O Java tem duas funções diferente como heap e pilha, então o java cria referênciais espalhadas e não empilhadas como
pulha, sendo portanto mais organizada e ágil.

Comparando objetos semelhantes, usa-se o equals.

# String

São tipos básicos, portanto o java as trata de maneira diferente e vão para uma área específico "pool de string" e são
imutávies.

# Concatenando strings de maneira eficiente

Primeiramente, quando fazemos a concatenação, a string novas são criadas dentro do pool, não juntando as palavras.

Exemplo loop for.

Melhor resposta, utilização do SpringBuilder, este é um objeto mutável que contrui o objeto que é modificado ao longo do
tempo, sendo eficiente e limpando o pool.

Obse: StringBuilder para trabalhar com concatenação de forma mais eficiente do que com as Strings tradicionais. Porém, a
classe StringBuilder não é o que chamamos de thread-safe, ou seja, não é seguro trabalhar com threads utilizando a
classe StringBuilder, pois ela não sincroniza os dados.
Deve-se usar a StringBuffer.

# Out of memory erro

Há um espaço na heap do java - erro em heap - conhecido como estouro de memória.

Como resolver ? Usando page para paginação de dados o que limita a memória.

Em situações diferente, o que fazer:
Falar para o s.o alocar mais memória.
No intelij é diferente:
Em configurações da jvm, devo port -Xmx1G --> o final é o tamanho da memória.

Olá!   É muito bom te ver por aqui! Essa aula fala sobre os argumentos da JVM, que são como "instruções" que você pode
dar para o Java antes de ele executar seu programa. Eles são usados para configurar coisas como a quantidade de memória
que o Java pode usar (heap) e o tamanho da pilha para cada thread. A aula explica os argumentos mais importantes, como
-Xms, -Xmx e -Xss, e te incentiva a explorar a documentação da Oracle para aprender mais sobre outros argumentos. Você
tem alguma dúvida específica sobre esses argumentos? Fico feliz em te ajudar!

# Recurso java

Gargant collector - Mecanismo do Java que busca gagálos e classes morta para otimizar.

O nome do recurso do Java que é responsável por liberar a memória que não está mais sendo utilizada é Garbage Collector,
ou Coletor de Lixo em português.

Ele é como um "faxineiro" da memória, que fica limpando os objetos que não estão mais sendo usados, para que a memória
fique livre para novos objetos.

Você pode pensar no Garbage Collector como um robô que anda pela sua casa e recolhe o lixo que você não está mais
usando. Ele faz isso para que a sua casa fique organizada e você tenha espaço para novas coisas.

O GC pode ser invocado.

A aula que você está estudando agora é sobre o Garbage Collector e como ele funciona no Java.

O Garbage Collector é como um "faxineiro" que cuida da memória do seu programa. Ele identifica os objetos que não estão
mais sendo usados e os remove da memória, liberando espaço para novos objetos.

Essa aula te ensina sobre o G1, um algoritmo de Garbage Collector que é muito eficiente e usado por padrão no Java 9 e
versões posteriores.

Você aprendeu que o G1 divide a memória em diferentes áreas: Eden Space, Survivor Space e Old Generation.

Cada objeto criado é inicialmente alocado no Eden Space. Se ele sobreviver a algumas coletas de lixo, ele é movido para
o Survivor Space. E se ele continuar sendo usado por muito tempo, ele vai para a Old Generation. 