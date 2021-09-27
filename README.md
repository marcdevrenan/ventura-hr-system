# VenturaHR

## Descrição do Projeto
Projeto arquitetado e desenvolvido com intuito de otimizar e inovar o sistema de processo seletivo realizado por empresas em busca de candidatos.

## 🚀 Status do Projeto
🚧 Em construção... 🚧

### Features ✅
- [x] Usuário - Manter Usuário
- [x] Usuário - Logar no Site
- [x] Empresa - Publicar Vaga
- [x] Empresa - Listar Vagas Publicadas
- [x] Usuário - Pesquisar Vagas
- [x] Candidato - Responder Vaga
- [x] Candidato - Listar Vagas Respondidas
- [ ] Empresa - Consultar Ranking
- [ ] Empresa - Consultar Dados do Candidato

## 📦 Pré-requisitos
Antes de começar, será necessário ter instalado na máquina o [Git](https://git-scm.com/), [PostgreSQL](https://www.postgresql.org/download/) e [Tomcat](http://tomcat.apache.org/).
Além disto é bom ter um editor de sua preferência para trabalhar com o código, como por exemplo o [NetBeans](https://netbeans.apache.org/).

```bash
# Clone este repositório
$ git clone<https://github.com/marcdevrenan/ventura-hr-system.git>
```

### 🛠 Tecnologias
As seguintes ferramentas foram usadas na construção do projeto:

- [Java 11](https://www.oracle.com/java/technologies/javase/jdk11-archive-downloads.html)
- [IntelliJ IDEA](https://www.jetbrains.com/idea/download/#section=windows)
- [PostgreSQL](https://www.postgresql.org/download/)
- [pgAdmin](https://www.pgadmin.org/download/)
- [Postman](https://www.postman.com/downloads/)

## 📝 Relatório de Desenvolvimento
Inicialmente o projeto foi proposto para desenvolvimento ao longo de 6 meses, sendo diluído em etapas de construção, buscando flexibilizar a curva aprendizado/implementação.

O projeto VenturaHR teve como proposta a base de um modelo de microsserviços, que trata da aplicação como um conjunto de serviços que se comunicam através de chamadas de forma assíncrona, onde os módulos são totalmente independentes um do outro para operar, dando assim uma grande capacidade de escalonamento horizontal, facilitando a manutenção e o enriquecimento do mesmo.

Durante os 3 primeiros meses do processo, realizamos o estudo de casos de uso, diagramação, documentação e por fim teorizamos por meio de exemplos isolados como deveria ser construída a aplicação, metodologia essa que mistura um pouco de cascata com desenvolvimento ágil, pois devido ao processo realizado em etapas pôde-se compreender que nem tudo o que foi pensado pôde de fato ser aplicado, alguns por questões de dificuldade e curva de aprendizado e outros por conflitos que seriam gerados dentro do próprio sistema.

O processo de construção e implementação do sistema consumiu boa parte do tempo em realizar as funções previstas com base no modelo de microsserviços instituído no início da aplicação, tendo assim uma composiçaõ de projetos não só logicamente como fisicamente isolados, o que trouxe grande complexidade no seu desenvolvimento no ato de enviar e receber dados entre um serviço e outro.

Cito aqui que a arquitetura original previa a utilização de servlets para gerir os controladores e o módulo web da aplicação, onde eu optei por fazer com o Spring Boot, me proporcionando uma certa uniformidade entre API's e Web.

A construção do banco de dados se deu através da própria aplicação utilizando as anotações do Spring, oque teve seu processo de adaptação inicial, desde a aquisição dos recursos necessários para que pudesse funcionar em harmonia com o sistema até o input correto dos dados nas tabelas.

Por fim diversos recursos foram adaptados de seus formatos originais, visando melhorias na implementação e também otimização do próprio sistema. Esta etapa colocou em prática todos os fundamentos estudados previamente e a capacidade de desvendar e solucionar problemas, assim como prever certas condições indesejáveis para o futuro cliente da aplicação.

Durante o processo mantive meu foco no primordial da aplicação, no que de fato tornaria ela um instrumento de avaliação, logo, descartei a intenção em aplicar o desenvolvimento em nuvem e também o tratamento do front-end com alguma ferramenta mais adequada.

### 🐛 Bugs
Devido ao uso recorrente de rotas entre diferentes chamadas de métodos,  passando path e chamando telas, a aplicação se encontra em um estado confuso de organização, onde alguns métodos acabam se repetindo por um processo de "cobertura de imprevistos", ao qual foi uma tentativa de blindar a ineficiência operacional provida pela desordem das rotas.

Outra questão importante foi a perda de sessão temporária ao jogar o usuário diretamente da criação de conta para dentro do sistema, onde o mesmo ao realizar uma de suas ações acaba perdendo sua identidade (id), o que acarretou em erros internos principalmente na publicação de novas vagas, onde uma vaga requer a associação direta a um usuário que esta a criando.

De forma geral lidar com front e back ao mesmo tempo me trouxe alguns problemas, pois a forma como um dado se apresenta na tela nem sempre é a forma como o sistema espera armazená-lo, o que inside alguns processos de tratamento daquela informação para que então ela esteja adequada ao controlador.

## 💻 Autor
- Armênio Torres - Arquiteto, professor e orientador do sistema.
- [Renan Ferreira Marcílio](https://www.linkedin.com/in/renan-ferreira-1175541a3/) - Aluno e desenvolvedor do projeto.

## 📖 Licença
[JetBrains Educational](https://www.jetbrains.com/community/education/#students)