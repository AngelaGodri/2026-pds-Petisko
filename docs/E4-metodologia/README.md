A metodologia adotada desempenha um papel crucial no desenvolvimento do sistema PE2Tisko. Este capítulo apresenta a abordagem utilizada para planejar, implementar e testar o sistema, além de destacar as ferramentas, tecnologias e materiais empregados durante o processo. A seguir, são detalhadas a abordagem de desenvolvimento, as ferramentas e tecnologias utilizadas, e a arquitetura do sistema, proporcionando uma visão abrangente do processo de criação deste sistema web. 

Abordagem de Desenvolvimento 

Para o desenvolvimento do sistema web PETisko, foi adotada uma abordagem ágil de desenvolvimento de software baseada no framework Scrum, combinada com práticas do Kanban para o gerenciamento visual de tarefas. 

O ciclo de vida do projeto foi estruturado em iterações curtas e contínuas (Sprints) com duração de duas semanas cada. A cada Sprint, o conjunto de requisitos prioritários do Product Backlog — tais como a carteirinha digital, o mural de busca por geolocalização e a central de artigos — foi planejado, implementado, testado e validado de forma iterativa e incremental. 

Durante as iterações, foram realizadas reuniões de alinhamento (Daily Meetings) para acompanhamento do progresso diário e rápida remoção de impedimentos, além de rituais de Sprint Planning no início de cada ciclo e Sprint Review ao final, garantindo a evolução constante e a qualidade das entregas. Justificativa da Escolha: 

A escolha da metodologia ágil baseada no Scrum/Kanban justifica-se pela necessidade de flexibilidade e rápida adaptação diante dos requisitos multifacetados da plataforma PETisko. Por se tratar de um sistema que engloba diferentes módulos operacionais (gestão sanitária, mapa interativo, mural colaborativo em tempo real e controle de perfis), a abordagem incremental permitiu: 

 Entregas de Valor Frequentes: Validação antecipada dos módulos mais críticos (como o cadastro de pets e o alerta de animais perdidos) antes da integração total da plataforma. 

Mitigação de Riscos: Identificação e correção ágil de falhas de arquitetura, banco de dados ou navegação a cada término de Sprint. 

 Gerenciamento Visual e Organização: O uso do quadro Kanban permitiu transparência total sobre o fluxo de desenvolvimento de cada caso de uso (A Fazer, Em Desenvolvimento, Em Teste e Concluído), otimizando o tempo da equipe e assegurando o cumprimento dos prazos estabelecidos. 

Ferramentas e Tecnologias 

As principais ferramentas e tecnologias utilizadas no desenvolvimento do sistema foram: 

HTML: É a estrutura do site. Define textos, títulos, imagens, botões, formulários, menus e outras partes da página. 

CSS: É responsável pela aparência do site. Define cores, fontes, tamanhos, espaçamentos, posicionamento e responsividade. 

JavaScript: Adiciona interatividade ao site. Pode controlar botões, formulários, menus, mapas, atualizações de conteúdo e outras ações sem precisar recarregar a página. 

Python: Linguagem utilizada principalmente no back-end, responsável pela lógica do sistema, processamento de informações e comunicação com o banco de dados. 

SQL: Linguagem usada para trabalhar com bancos de dados. Permite inserir, consultar, alterar e excluir informações armazenadas no sistema. 

Flask: Framework de Python utilizado para criar o servidor e o back-end do site. Ele conecta as páginas HTML à lógica do sistema e ao banco de dados. 

Bootstrap: Framework de CSS que facilita a criação do visual do site. Possui componentes prontos, como botões, menus, formulários e sistemas de colunas, além de ajudar na adaptação para celulares. 

Jinja2: Sistema de templates utilizado pelo Flask. Permite colocar informações vindas do Python diretamente nas páginas HTML, como nomes de usuários, produtos ou resultados de pesquisas. 

Visual Studio Code: Editor de código utilizado para escrever e organizar os arquivos HTML, CSS, JavaScript, Python e outros arquivos do projeto. 

Git: Sistema de controle de versões. Permite registrar as alterações feitas no projeto e voltar para versões anteriores caso aconteça algum problema. 

GitHub: Plataforma para armazenar o código do projeto online utilizando Git. Também facilita o trabalho em equipe e o compartilhamento do código. 

Navegador web (Google Chrome, por exemplo) 
Usado para acessar e testar o site. É nele que o usuário visualizará as páginas e utilizará as funcionalidades do sistema. 

Cloudflare: Pode atuar como uma camada entre o usuário e o servidor, oferecendo recursos como DNS, segurança, proteção contra ataques e gerenciamento de tráfego. 

Leaflet: Biblioteca JavaScript utilizada para criar mapas interativos no site. Permite mostrar mapas, marcadores, locais e outras informações geográficas. 

Servidor local Flask: É o servidor utilizado durante o desenvolvimento. Permite executar o sistema no próprio computador para testar as páginas, funcionalidades e banco de dados antes de publicar o site. 
Hospedagem em nuvem (Render, por exemplo). Permite colocar o site em um servidor disponível pela internet, possibilitando que outras pessoas acessem o sistema. 

MySQL: Sistema de gerenciamento de banco de dados. Será utilizado para armazenar informações do site, como usuários, cadastros, locais, produtos ou outros dados do sistema. 

 

Arquitetura do Sistema 

A arquitetura do sistema PETisko segue o modelo Cliente-Servidor (Client-Server) com uma separação clara de responsabilidades (Separation of Concerns) entre a camada de apresentação (Frontend), a camada de aplicação e regras de negócio (Backend) e a camada de persistência de dados (Database). 

Frontend (Camada de Apresentação): 

A interface com o usuário é estruturada seguindo o padrão de Arquitetura Baseada em Componentes. A aplicação web/mobile responsiva é responsável por renderizar as telas do sistema, como o mural de busca por geolocalização, a carteirinha digital do pet e o painel administrativo. Ela interage com o servidor por meio de requisições assíncronas via API REST (JSON), permitindo uma navegação fluida e sem recarregamento total das páginas. 

  

Backend (Camada de Aplicação e Lógica de Negócio): 

O servidor backend adota o padrão arquitetural MVC (Model-View-Controller) / Layered Architecture (Arquitetura em Camadas), organizado nas seguintes divisões: 

  

Controller (Rotas e Endpoints): Recebe as requisições HTTP do frontend, valida as entradas e direciona para as regras de negócio. 

  

Service/Business Logic (Lógica de Negócio): Executa as regras da aplicação, como validação de idade mínima para cadastro, controle de status do alerta de pet perdido e agendamento automático de lembretes sanitários. 

  

Model (Persistência e Acesso aos Dados): Mapeia as entidades do banco de dados (Tutor, Pet, Alerta, Estabelecimento, etc.) e gerencia as operações de inserção, leitura, atualização e exclusão (CRUD). 

  

Banco de Dados (Camada de Persistência): 

A persistência das informações utiliza um Sistema Gerenciador de Banco de Dados Relacional (SGBDR). O modelo relacional assegura a integridade referencial por meio de chaves primárias (PK) e estrangeiras (FK), garantindo a rastreabilidade total entre tutores, pets, históricos médicos e alertas do mural. 

  

Princípios de Design e Decisões Arquiteturais 

A construção da arquitetura do PETisko foi norteada pelos seguintes princípios fundamentais de engenharia de software: 

  

Baixo Acoplamento e Alta Coesão: Módulos independentes permitem que alterações no módulo de Geolocalização ou na Página Informativa não afetem o funcionamento do módulo de Carteirinha do Pet. 

  

Segurança e Autenticação: Adoção de autenticação baseado em tokens seguros (JWT — JSON Web Token) para proteger as rotas privadas (como edição de perfil e carteirinha) e criptografia com algoritmo de hash seguro para armazenamento de senhas dos usuários. 

  

Acessibilidade Pública Parcial: Decisão de design que permite ao usuário sem autenticação (Visitante) o acesso direto à leitura das APIs do mural de busca e do mapa de estabelecimentos, garantindo agilidade no resgate de animais sem criar barreiras de login. Conforme pode ser observado na Figura 1, a arquitetura do sistema está estruturada da seguinte forma: 

Padrão: Cliente-Servidor 

Padrão: Cliente-Servidor (Client-Server) 

Frontend: 

Tecnologia: React.js / HTML5 + CSS3 / JavaScript 

Arquitetura: Componentes (Component-Based) 

 

Backend: 

Arquitetura: MVC (Model-View-Controller) 

Tecnologia: Node.js com Express.js 

Banco de Dados: PostgreSQL / MySQL (SGBD Relacional) 

Comunicação com o banco de dados: Driver oficial do SGBD / ORM (Sequelize/Prisma) 

 

Componentes: 

Cliente (Módulo Web e Móvel): Interfaces web e responsivas para interação do Tutor, Administrador e Visitante com a aplicação. 

Servidor (Módulo de Controle/Backend): Processamento das requisições HTTP, autenticação, execução das regras de negócio (alertas, lembretes) e mediação do acesso ao banco de dados. 

Banco de Dados: Armazenamento persistente e relacional das informações de tutores, pets, históricos médicos, alertas de desaparecimento, artigos e estabelecimentos. 

 

Fluxo de Informação: 

O Cliente (Tutor, Visitante ou Administrador) interage com a interface (Módulo Web/Móvel) e envia uma requisição HTTP para o servidor. 

O Módulo de Controle (Servidor Backend) recebe a requisição, processa a regra de negócio e solicita ou persiste os dados necessários no Banco de Dados. 

O Banco de Dados executa a instrução SQL e devolve os dados para o Módulo de Controle. 

O Módulo de Controle formata os dados em resposta JSON e os devolve para o Cliente, que atualiza a interface para o usuário. 

 A imagem apresentada, figura 2, segue os seguintes contextos: 

Atores externos: Posiciona o Tutor, Administrador e Visitante no topo e laterais interagindo diretamente com a interface. 

 

Caixa do Sistema: Delimita a fronteira do sistema PETisko englobando a Interface, o Módulo de Controle (Backend) e o ícone de cilindro oficial para o Banco de Dados. 

  

Fluxo bidirecional: As setas de idas e voltas representam as requisições e respostas do fluxo de informação.

 
