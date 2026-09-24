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

## Criação do ambiente virtual e instalação

Com o `uv`, a criação da `.venv` e a instalação de todas as dependências declaradas no `pyproject.toml` ocorrem em uma única etapa:

```powershell
cd setup
uv sync
```

O `uv` identificará a versão do Python fixada em `.python-version` (3.12.1), criará a pasta `.venv/` e instalará:

- **pandas** e **pyarrow**: bibliotecas principais para manipulação de dados tabulares.
- **ipykernel**: suporte para execução dos Jupyter Notebooks.
- **nbstripout**: ferramenta de limpeza de saídas de notebooks para commits limpos no Git.

## Registro do Kernel para Jupyter Notebooks

Para que qualquer editor (VS Code, Cursor, Antigravity) conecte os notebooks aos pacotes instalados nesta `.venv`, execute:

```powershell
uv run python -m ipykernel install --user --name project_tasks_pandas --display-name "Python (project_tasks_pandas)"
```

## Ativação manual (Opcional)

Se preferir usar o terminal com o ambiente ativado tradicionalmente:

```powershell
.\.venv\Scripts\Activate.ps1
```

Caso o PowerShell bloqueie a execução de scripts:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy Bypass
.\.venv\Scripts\Activate.ps1
```

## Gerenciamento de dependências

Para adicionar novas bibliotecas ao projeto:

```powershell
uv add nome-da-biblioteca
```

## Executar o script de teste

Para validar que o ambiente está funcional:

```powershell
uv run python main.py
```
