# Setup do ambiente

Este projeto utiliza **Python 3.12.1** e **uv** para criação e gerenciamento do ambiente virtual.

O arquivo `.python-version`, na raiz do repositório, fixa a versão `3.12.1`. O arquivo `pyproject.toml`, dentro desta pasta `setup`, concentra as configurações do projeto Python.

## Pré-requisitos

- Python 3.12.1 instalado
- uv instalado

Para conferir as versões:

```powershell
python --version
uv --version
```

## Criar o ambiente virtual

Entre na pasta `setup`:

```powershell
cd setup
```

Crie o ambiente virtual `.venv`:

```powershell
uv venv .venv
```

Ative o ambiente no PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

Caso o PowerShell bloqueie a ativação do ambiente, execute:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
```

## Instalar dependências

Com o ambiente ativado, sincronize as dependências declaradas no `pyproject.toml`:

```powershell
uv sync
```

No estado atual, o projeto utiliza a biblioteca **pandas** para manipulação e análise de dados tabulares.

Para adicionar novas dependências futuramente, utilize:

```powershell
uv add nome-da-biblioteca
```

## Executar o projeto de setup

Ainda dentro da pasta `setup`, execute:

```powershell
uv run python main.py
```
