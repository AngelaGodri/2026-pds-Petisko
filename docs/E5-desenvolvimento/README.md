Neste capítulo, detalhamos o processo de criação do sistema PETisko, desde a sua concepção inicial até as fases de modelagem e planejamento da entrega final. Serão apresentadas as etapas de descrição do projeto, análise detalhada do sistema, arquitetura da aplicação, implementação das funcionalidades e realização de testes para garantir a qualidade, segurança e eficiência da plataforma desenvolvida. Este capítulo oferece uma visão abrangente do trabalho prático envolvido na construção do sistema PETisko, fornecendo insights valiosos sobre o processo de desenvolvimento de software aplicado à causa e ao bem-estar animal. 

Descrição do Projeto 

O PETisko é uma aplicação web desenvolvida com o objetivo de centralizar e organizar a jornada de cuidado e proteção com os animais de estimação. A plataforma foi idealizada para atender a duas demandas principais enfrentadas por tutores e pela comunidade: a desorganização e perda de alcance na busca por animais desaparecidos e a dispersão de informações essenciais de saúde e serviços veterinários. 

 Para atender a esses desafios, o projeto contempla quatro eixos funcionais principais: 

Rede Colaborativa de Pets Perdidos e Encontrados: Módulo em tempo real para cadastro, divulgação e consulta georreferenciada de animais desaparecidos na região. 

Prontuário e Histórico de Saúde Digital: Ambiente restrito e autenticado para o gerenciamento de vacinas, consultas, exames, alergias e lembretes sanitários do animal. 

Mapeamento de Serviços Veterinários: Integração com serviços de localização por mapa para identificação rápida de clínicas veterinárias, plantões emergenciais e pet shops próximos. 

Central Informativa de Cuidados Básicos: Página de consulta interativa para orientações ágeis sobre posse responsável e primeiros cuidados. 

Análise do Sistema 

Para a análise do sistema PETisko, utilizamos a linguagem de modelagem UML (Unified Modeling Language) para representar os requisitos, comportamentos e a estrutura da aplicação. Adotamos uma abordagem ágil baseada no framework Scrum, que inclui a definição e gerenciamento do Product Backlog, Sprint Backlog e Daily Scrum, facilitando o desenvolvimento iterativo e incremental da plataforma web de monitoramento e proteção pet. 

 

Product Backlog: No Product Backlog, foram listadas todas as funcionalidades desejadas para o sistema, priorizadas de acordo com o valor gerado para os tutores, clínicas veterinárias e para a comunidade de apoio animal. Exemplos de itens do Product Backlog incluem: cadastro de usuários e perfis dos pets, gerenciamento do prontuário médico digital (vacinas, exames, alergias e consultas), módulo de lembretes e notificações sanitárias, publicação e consulta georreferenciada de alertas de pets perdidos/encontrados em tempo real, integração com mapas para localização de clínicas/pet shops e a central de orientação interativa com suporte de inteligência artificial. 

Sprint Backlog: Durante o planejamento de cada Sprint, selecionamos um conjunto de itens do Product Backlog para serem implementados na iteração vigente. Esses itens foram detalhados no Sprint Backlog, onde foram divididos em tarefas menores (como modelagem de tabelas do banco de dados, criação de telas de cadastro, integração com APIs de mapas e desenvolvimento de rotas de autenticação) e estimados em termos de esforço e complexidade técnica para sua conclusão. 

Daily Scrum: Durante o Daily Scrum, realizamos alinhamentos de curta duração entre a equipe de desenvolvimento para sincronizar o progresso dos módulos e identificar quaisquer impedimentos técnicos. Nessas reuniões, a equipe discutiu o que foi implementado desde o encontro anterior, as metas a serem cumpridas até a próxima sessão (como ajustes em regras de negócio ou correções de interface) e os eventuais obstáculos que precisavam de solução imediata. 

A abordagem Scrum aliada à modelagem UML permitiu uma análise detalhada e uma gestão eficaz do desenvolvimento do sistema PETisko, garantindo a entrega contínua de valor à comunidade e flexibilidade para adaptações ao longo do ciclo de vida do projeto. 

Levantamento de Requisitos 

Para a etapa de levantamento de requisitos do projeto PETisko, adotou-se a técnica de Questionário, caracterizada pela aplicação de formulários virtuais estruturados (via Google Forms) para a coleta assíncrona de dados quantitativos e qualitativos em escala. Esta abordagem mostrou-se ideal para abranger de forma rápida a diversidade e a realidade dos principais stakeholders do projeto: tutores de animais, proprietários de clínicas veterinárias/pet shops e representantes de comunidades, ONGs e protetores independentes. A aplicação foi realizada por meio digital, em que formulários personalizados são compartilhados com questões especificas para mapear suas necessidades detalhada quanto ao monitoramento de saúde, geolocalização e à divulgação de animais perdidos. 

A seguir, são apresentados os Requisitos Funcionais Identificados:  

− RF01 - O sistema deve mostrar uma página de cadastro que informe o nome de usuário, email, senha, endereço, número de telefone e idade(+13). 

− RF02 - O sistema deve permitir uma página de login que informe o e-mail, nome e senha cadastrados para logar. 

− RF03 - O sistema deve permitir mostrar uma página com as informações do usuário. 

− RF04 - O sistema deve permitir que um usuário não autenticado(visitante), possa acessar o mural de pets perdidos e divulgar a busca do pet na plataforma sem a necessidade de realizar cadastro ou login. 

− RF05 - O sistema deve disponibilizar uma aba para página de cadastro do pet que contenha o nome do animal de estimação, idade, data de nascimento, raça, espécie, sexo, peso, nome do tutor. 

− RF06 - O sistema deve permitir que o veterinário registre e consulte o histórico médico do pet, e atualize os dados de vacinas tomadas, exames, consultas e alergias. 

− RF07 - O sistema deve possibilitar a visualização e emissão da carteirinha digital de vacinação e saúde do pet cadastrado. 

− RF08 - O sistema deve emitir lembretes e notificações de compromissos de cuidados, como datas de retorno de vacinas, vermífugos e consultas agendadas. 

− RF09 - O sistema deve permitir uma página para cadastrar um alerta/informações do pet perdido que contenha: nome do pet, imagem do pet, descrição do pet, número de telefone do tutor, localização do desaparecimento/resgate. 

− RF10 - O sistema deve exibir um mural colaborativo em tempo real com todos os alertas de animais perdidos e encontrados ativos na plataforma. 

− RF11 - O sistema permite a filtragem no mural colaborativo de anúncios de pets perdidos/resgatados, que seleciona critérios como cidade, bairro, espécie e período do desaparecimento. 

− RF12 - O sistema deve exibir uma página na lateral da tela, dividida em tópicos nos seguintes tópicos de informações: nutrição, higiene, vacinação e posse responsável de animais de estimação.  

− RF13 - O sistema deve permitir a navegação por categorias temáticas de cuidados (ex.: cães, gatos, filhotes, animais idosos e emergências/primeiros socorros). 

− RF14 - O sistema deve disponibilizar um painel administrativo exclusivo para que os administradores possam criar, editar, categorizar e remover os artigos e dicas informativas da plataforma 

− RF15 - O sistema deve exibir um mapa interativo com pontos com a imagem do lugar, que mostram a localização de clínicas veterinárias e pet shops. 

− RF16 - O sistema deve mostrar apenas os pontos de clínicas e petshops, que estão próximos ao usuário. 

− RF17 - O sistema deve permitir a consulta detalhada das informações dos estabelecimentos mapeados (endereço, telefone de contato e horário de funcionamento). 

A seguir são apresentados os Requisitos Não Funcionais Identificados:  

− RNF01 - Desempenho: O sistema deve apresentar tempo de resposta inferior a 2 segundos no carregamento das páginas principais e na execução de consultas e buscas. 

− RNF02 - Segurança: O acesso aos dados de saúde do pet e às informações do usuário deve ser restrito e protegido por autenticação, garantindo que apenas o tutor logado possa visualizar ou alterar suas informações. 

− RNF03 - Usabilidade: O sistema deve possuir uma interface responsiva, clara e de fácil navegação, adaptando-se automaticamente a diferentes tamanhos de tela (computadores, tablets e smartphones). 

− RNF04 - Compatibilidade: A aplicação web deve ser compatível com os principais navegadores de mercado (Google Chrome, Mozilla Firefox, Microsoft Edge e Safari). 

− RNF05 - O sistema de geolocalização deve ser integrado a APIs padrão de mapas digitais (como Leaflet ou Google Maps API), garantindo pleno funcionamento em navegadores modernos sem necessidade de plugins adicionais. 

− RNF06 - Disponibilidade: O sistema deve permanecer disponível para acesso 24 horas por dia, 7 dias por semana (24/7), garantindo suporte contínuo principalmente para a busca de pets perdidos e emergências veterinárias. 

− RNF07 - Conformidade Legal: O tratamento e o armazenamento dos dados pessoais dos usuários e tutores devem estar em conformidade com as diretrizes da Lei Geral de Proteção de Dados (LGPD). 

− RNF08 - Manutenibilidade: O código-fonte do sistema deve ser modular e documentado, facilitando correções, atualizações futuras e a inclusão de novas funcionalidades. 

 

 
