# Estudos de Pandas para análise e tratamento de dados

Este repositório reúne notebooks e materiais de estudo para praticar **Pandas** em fluxos comuns de análise e preparação de dados.

O objetivo é construir uma base de consulta prática para quem está aprendendo a trabalhar com dados tabulares em Python, passando por etapas como carregamento de arquivos, exploração inicial, diagnóstico da base, tratamentos básicos e criação de novas colunas.

## Objetivo do repositório

Este projeto serve como um espaço de estudo guiado para:

- praticar comandos essenciais do Pandas;
- organizar exercícios de curso;
- documentar o raciocínio por trás de cada etapa;
- criar notebooks reutilizáveis para consulta futura;
- ajudar outras pessoas de Data Analytics e Data Engineering a estudarem os mesmos conceitos.

## Estrutura do projeto

```text
.
├── data/
│   └── superstore.csv
├── setup/
│   ├── README.md
│   ├── main.py
│   ├── pyproject.toml
│   └── uv.lock
├── notebooks/
│   └── tasks_explore_format_data.ipynb
└── README.md
```

## Notebooks

### `notebooks/tasks_explore_format_data.ipynb`

Notebook voltado para os primeiros passos ao receber uma nova base de dados.

Ele funciona como um roteiro de exploração inicial, cobrindo pontos como:

- importação do Pandas;
- leitura de arquivo CSV;
- visualização inicial da base;
- inspeção de colunas e tipos de dados;
- estatísticas descritivas;
- verificação de valores nulos;
- padronização de nomes de colunas;
- análise de duplicidades;
- criação de novas variáveis.

A proposta é manter o notebook didático, com explicações e perguntas-guia, para que ele possa ser usado tanto como estudo pessoal quanto como material de apoio para outras pessoas.

## Base de dados

A pasta `data/` contém a base `superstore.csv`, usada nos exercícios iniciais do projeto.

Essa base é utilizada para praticar operações comuns em dados de vendas, como filtros por região, cálculo de vendas, lucro, desconto e criação de indicadores derivados.

## Ambiente do projeto

O projeto utiliza:

- Python 3.12.1
- uv
- Pandas
- nbstripout

As configurações do ambiente ficam na pasta `setup/`.

## Primeiros passos

Para preparar o ambiente, acesse a pasta `setup/` e sincronize as dependências:

```powershell
cd setup
uv sync
```

Depois, volte para a raiz do repositório e instale o filtro local do `nbstripout`:

```powershell
cd ..
uv --project setup run nbstripout --install
```

Esse filtro remove automaticamente outputs, contadores de execução e metadados voláteis dos notebooks quando eles são adicionados ao Git. Assim, os commits ficam focados no código e nas explicações das células.

Esse passo precisa ser feito uma vez por clone local do repositório.

Para mais detalhes, consulte o arquivo [setup/README.md](setup/README.md).

## Como usar este repositório

1. Prepare o ambiente Python seguindo as instruções da pasta `setup/`.
2. Abra os notebooks no Jupyter, VS Code ou outro ambiente compatível.
3. Execute as células na ordem.
4. Leia as perguntas-guia antes de escrever ou alterar código.
5. Use os exercícios do curso como prática e complemente com suas próprias análises.

## Próximos passos

Este repositório será expandido com novos notebooks de exercícios, conforme o curso disponibilizar novos desafios.

A ideia é manter cada notebook organizado por tema, com explicações suficientes para que outras pessoas também consigam estudar pelo material.
