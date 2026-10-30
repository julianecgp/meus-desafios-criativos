# Plano de Estudo Prático de Bancos de Dados & IA

Plano de estudo de 4 semanas (20 dias úteis) focado em **Bancos de Dados Relacionais (MySQL)**, **Não Relacionais (NoSQL)** e **Integração com Inteligência Artificial (IA)**, voltado para estudantes e recém-formados com ênfase prática em manipulação de dados.

---

## Tabela: Plano de Estudo Prático de Bancos de Dados & IA

| Dia/Semana | Tema Principal | Tópicos Específicos do Dia | Atividade Prática - Mão na Massa (com foco em manipulação de dados e IA) | Carga Horária Estimada (até 5h) |
| :--- | :--- | :--- | :--- | :--- |
| **Semana 1 - Dia 01** | MySQL: Fundamentos e Modelagem | DDL, tipos de dados, chaves primárias e estrangeiras, normalização (1FN a 3FN), índices primários. | Criar o schema relacional de uma plataforma e usar IA generativa (via prompt engineering estruturado) para gerar scripts de povoamento com dados sintéticos realistas. | 3h 30min |
| **Semana 1 - Dia 02** | MySQL: DML e Consultas Essenciais | `INSERT`, `UPDATE`, `DELETE`, `SELECT`, filtros com `WHERE`, operadores lógicos, ordenação e limites. | Executar manipulação de registros e construir scripts de limpeza de dados inconsistentes gerados na base sintética anterior. | 3h 00min |
| **Semana 1 - Dia 03** | MySQL: Consultas Avançadas e Agregações | `JOINs` (INNER, LEFT, RIGHT), `GROUP BY`, `HAVING`, funções de agregação (`COUNT`, `SUM`, `AVG`), CTEs (`WITH`). | Escrever queries analíticas para extração de métricas de negócio e utilizar assistentes de IA para refatorar queries lentas e explicar o plano de execução (`EXPLAIN`). | 4h 00min |
| **Semana 1 - Dia 04** | MySQL: Transações, Integridade e Triggers | Propriedades ACID, níveis de isolamento, `COMMIT`/`ROLLBACK`, criação de Triggers e Views. | Implementar uma Trigger de auditoria de alterações de dados e testar integridade transacional simulando falhas de execução. | 3h 30min |
| **Semana 1 - Dia 05** | Integração MySQL + IA (Text-to-SQL) | Conexão Python com MySQL (`mysql-connector` ou `SQLAlchemy`), arquitetura de Text-to-SQL. | Desenvolver um pipeline em Python que recebe perguntas em linguagem natural, converte em SQL usando API de LLM e executa a query com sanitização básica. | 4h 30min |
| **Semana 2 - Dia 06** | NoSQL: Modelo de Documentos (MongoDB) | Teorema CAP, NoSQL vs Relacional, estrutura BSON/JSON, coleções e flexibilidade de schema. | Instalar e configurar MongoDB localmente/Docker, modelando um catálogo de produtos semi-estruturado com atributos dinâmicos. | 3h 00min |
| **Semana 2 - Dia 07** | NoSQL: CRUD e Filtros no MongoDB | Operadores de consulta (`$eq`, `$gt`, `$in`, `$regex`), operadores de atualização (`$set`, `$push`), índices. | Manipular documentos semiestruturados via Python (`pymongo`), realizando buscas textuais e atualizações em lote de documentos complexos. | 3h 30min |
| **Semana 2 - Dia 08** | NoSQL: MongoDB Aggregation Framework | Estágios de pipeline (`$match`, `$group`, `$project`, `$unwind`, `$lookup`), transformações de dados. | Construir um pipeline de agregação para consolidação de métricas comportamentais a partir de logs em formato JSON. | 4h 00min |
| **Semana 2 - Dia 09** | NoSQL: Chave-Valor com Redis | Estruturas de dados em memória (Strings, Hashes, Lists, Sets), expiração (TTL), estratégias de cache. | Implementar camada de cache em Redis com Python para armazenar resultados de consultas pesadas do MySQL e do MongoDB. | 3h 30min |
| **Semana 2 - Dia 10** | NoSQL + IA: Ingestão e Estruturação de Dados | Extração de entidades (NER), parsing de texto desestruturado para JSON via LLM. | Criar um script que lê feedbacks de clientes em texto livre, usa IA para extrair sentimento e palavras-chave em formato JSON estruturado, salvando no MongoDB. | 4h 00min |
| **Semana 3 - Dia 11** | Bancos Vetoriais: Teoria e Vetorização | Conceito de Vetores e Embeddings, métricas de distância (Cosseno, Euclidiana, Dot Product). | Gerar embeddings vetoriais de textos técnicos usando modelos pré-treinados em Python e calcular similaridade semântica manualmente via matrizes. | 3h 30min |
| **Semana 3 - Dia 12** | Bancos Vetoriais Nativos (ChromaDB / Qdrant) | Arquitetura de Vector DBs, coleções, indexação vetorial, metadados associados a vetores. | Configurar o ChromaDB/Qdrant, indexar centenas de documentos textuais com metadados e realizar buscas por similaridade semântica. | 4h 00min |
| **Semana 3 - Dia 13** | Busca Vetorial Híbrida em NoSQL/Relacional | Extensões vetoriais modernas (MongoDB Atlas Vector Search ou MySQL HeatWave/vetores). | Configurar busca vetorial e executar queries híbridas: filtragem relacional/metadado combinada com ranking por proximidade semântica. | 4h 30min |
| **Semana 3 - Dia 14** | Pipeline de RAG (Busca e Geração Aumentada) | Estratégias de chunking de dados, indexação, recuperação de contexto e montagem de prompts. | Construir um pipeline RAG em Python que busca contexto em um banco vetorial/NoSQL e alimenta uma LLM para responder perguntas precisas sobre dados da empresa. | 4h 30min |
| **Semana 3 - Dia 15** | Otimização e Indexação em Bancos Vetoriais | Índices HNSW (*Hierarchical Navigable Small World*), trade-offs de precisão vs latência (*recall* vs *latency*). | Realizar benchmarks comparando tempo de resposta e acurácia de consultas com diferentes tamanhos de blocos (*chunks*) e índices vetoriais. | 4h 00min |
| **Semana 4 - Dia 16** | Persistência Poliglota e Arquitetura de Dados | Quando utilizar Relacional, Documento, Chave-Valor ou Vetorial; sincronização de dados. | Desenvolver um script integrador em Python: grava dados transacionais no MySQL, dados de sessão/cache no Redis e histórico/perfil no MongoDB. | 4h 00min |
| **Semana 4 - Dia 17** | Agentes de IA com Acesso a Bancos de Dados | *Function Calling* / *Tool Calling*, orquestração de ferramentas com LLMs (LangChain/LlamaIndex ou SDK nativo). | Criar um agente inteligente capaz de decidir dinamicamente se deve consultar o MySQL (dados financeiros) ou o NoSQL/Vetorial (base de conhecimento) para responder ao usuário. | 4h 30min |
| **Semana 4 - Dia 18** | Segurança, Governança e Validação de Queries | Riscos de injeção em Text-to-SQL, permissões de banco (Least Privilege), validação de schemas gerados por IA. | Construir um validador/sanitizador de SQL gerado por IA com restrição a comandos somente leitura (`SELECT`) e checagem de custo de query antes da execução. | 3h 30min |
| **Semana 4 - Dia 19** | Projeto Integrado (Parte 1): Modelagem e Ingestão | Integração ponta a ponta: DDL no MySQL, schemas flexíveis no MongoDB, coleções vetoriais. | Criar o pipeline completo de ingestão de dados de um sistema de suporte ao cliente: tickets relacionais no MySQL, histórico em JSON no MongoDB e base de artigos no Vector DB. | 4h 30min |
| **Semana 4 - Dia 20** | Projeto Integrado (Parte 2): Orquestração Inteligente | Consulta analítica automatizada, sumarização e relatórios assistidos por IA. | Finalizar e testar uma interface de consulta unificada via terminal/API em Python onde o usuário faz perguntas de negócio complexas e o sistema orquestra as consultas nos 3 bancos. | 5h 00min |

---

## Recomendações de Ferramentas para o Ambiente Prático

- **Bancos Relacionais:** MySQL 8.0+ (ou container Docker `mysql:8.0`) + DBeaver / MySQL Workbench.
- **Bancos NoSQL:** MongoDB Community Server ou Atlas + Redis CLI (ou container Docker `redis:alpine`).
- **Bancos Vetoriais:** ChromaDB (local/em memória) ou Qdrant.
- **Ecossistema Python:** Python 3.10+, `pymongo`, `mysql-connector-python`, `redis`, `chromadb`, e SDKs de LLM (`google-genai` ou `openai`).
