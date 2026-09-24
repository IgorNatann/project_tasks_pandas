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

Para preparar o ambiente e rodar os notebooks sem atritos, siga o passo a passo abaixo:

### 1. Sincronizar o ambiente com o `uv`

Acesse a pasta `setup/` e execute o `uv sync`. Isso criará a `.venv` automaticamente com todas as bibliotecas necessárias (Pandas, PyArrow, ipykernel, nbstripout):

```powershell
cd setup
uv sync
```

### 2. Registrar o Kernel do Jupyter

Para que qualquer editor (VS Code, Cursor, Antigravity) reconheça o ambiente nos notebooks imediatamente:

```powershell
uv run python -m ipykernel install --user --name project_tasks_pandas --display-name "Python (project_tasks_pandas)"
```

### 3. Ativar o filtro do `nbstripout` no Git

Volte para a raiz e registre o filtro para evitar commit acidental de saídas pesadas de notebooks:

```powershell
cd ..
uv --project setup run nbstripout --install
```

---

## Como usar os Notebooks

1. Abra qualquer notebook dentro da pasta `notebooks/` (por exemplo, `notebooks/tasks_explore_format_data.ipynb`).
2. No canto superior direito do editor, clique em **Select Kernel** -> **Jupyter Kernel...**.
3. Selecione o kernel **`Python (project_tasks_pandas)`**.
4. Execute as células normalmente!

Para detalhes adicionais sobre o gerenciamento de dependências, consulte [setup/README.md](setup/README.md).

## Próximos passos

Este repositório será expandido com novos notebooks de exercícios, conforme o curso disponibilizar novos desafios.

A ideia é manter cada notebook organizado por tema, com explicações suficientes para que outras pessoas também consigam estudar pelo material.
