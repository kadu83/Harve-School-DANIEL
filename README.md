# Harve School — Material de aulas

Este repositório reúne materiais de estudo de diferentes módulos da Harve School, com foco em análise de dados, Python, ETL e ferramentas de uso prático em sala de aula.

A ideia é que você consiga navegar facilmente entre as pastas por tema, por aula e por tipo de material, como notebooks, scripts e arquivos de dados.

---

## 🌐 O que há neste repositório

- [Exploração de Dados](Exploração%20de%20Dados/) — análise exploratória, estatística descritiva, visualização e exercícios práticos
- [Python_ETL](Python_ETL/) — ETL, automações, integração com bancos de dados e consumo de APIs
- [README.md](README.md) — guia de instalação, uso e referências complementares

---

## 📁 Como o material está organizado

A estrutura foi pensada para ser simples e didática:

- Cada tema ou disciplina tem sua própria pasta no nível raiz
- Dentro dela, existem pastas para cada aula
- Cada aula pode conter notebooks, scripts e dados

Exemplo:

```text
Harve-School/
  Exploração de Dados/
    Aula 1/
    Aula 2/
    Aula 3/
    EDA.ipynb
  Python_ETL/
    Aula 3/
    Aula 4/
    Harve_School_API_application.ipynb
    install.py
    FUNCTIONS_DICTIONARY.md
```

---

## 🚀 Como começar

1. Abra a pasta do projeto no VS Code
2. Escolha a disciplina que deseja estudar
3. Abra o notebook ou o script da aula correspondente
4. Execute os exemplos na ordem sugerida

Se estiver começando agora, uma boa ordem é:

- Para análise de dados: [Exploração de Dados/EDA.ipynb](Exploração%20de%20Dados/EDA.ipynb)
- Para ETL e automações: [Python_ETL/Aula 4/01_exportando_csv/exportando_csv.py](Python_ETL/Aula%204/01_exportando_csv/exportando_csv.py)

---

## 🧰 Instalação do Python e do pip

### Windows

1. Baixe o Python em: https://www.python.org/downloads/
2. Durante a instalação, marque a opção “Add Python to PATH”
3. Finalize a instalação e abra um novo terminal
4. Verifique se o Python está instalado:

```powershell
python --version
python -m pip --version
```

Se o comando `pip` não estiver disponível, use:

```powershell
py -m ensurepip --upgrade
py -m pip install --upgrade pip
```

### macOS

```bash
brew install python
python3 --version
python3 -m pip --version
```

Se o `pip` não estiver disponível:

```bash
python3 -m ensurepip --upgrade
python3 -m pip install --upgrade pip
```

### Linux (Ubuntu/Debian)

```bash
sudo apt update
sudo apt install python3 python3-pip -y
python3 --version
python3 -m pip --version
```

Se necessário:

```bash
python3 -m ensurepip --upgrade
python3 -m pip install --upgrade pip
```

> Dica: em alguns sistemas, o comando pode ser `python` ou `python3`. Use o que estiver disponível no seu terminal.

---

## 🧪 Criando um ambiente virtual

Um ambiente virtual ajuda a organizar as bibliotecas por projeto e evita conflitos entre aulas.

### Windows PowerShell

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
```

### Windows CMD

```cmd
python -m venv .venv
.\.venv\Scripts\activate.bat
```

### macOS/Linux

```bash
python3 -m venv .venv
source .venv/bin/activate
```

Para confirmar que o ambiente ativou, rode:

```bash
python --version
```

Se estiver usando PowerShell e tiver problema de permissão para ativar o ambiente, execute:

```powershell
Set-ExecutionPolicy -Scope Process -ExecutionPolicy RemoteSigned
```

---

## 📦 Instalando bibliotecas úteis

Depois de ativar o ambiente virtual, instale as bibliotecas que serão usadas nas aulas:

```bash
pip install --upgrade pip
pip install pandas matplotlib seaborn requests sqlalchemy pymysql python-dotenv jupyterlab
```

Se quiser uma versão mais enxuta para começar:

```bash
pip install pandas matplotlib jupyterlab
```

---

## 🐼 Pequeno tutorial de pandas

O pandas é uma biblioteca essencial para trabalhar com tabelas, CSV, Excel e análise de dados.

### 1. Importar a biblioteca

```python
import pandas as pd
```

### 2. Ler um arquivo CSV

```python
df = pd.read_csv('dados.csv')
print(df.head())
```

### 3. Verificar o tipo de dados

```python
print(df.info())
```

### 4. Selecionar colunas

```python
coluna = df['nome_da_coluna']
print(coluna.head())
```

### 5. Filtrar linhas

```python
subset = df[df['idade'] > 30]
print(subset.head())
```

### 6. Agrupar dados

```python
df.groupby('categoria')['valor'].sum()
```

### 7. Criar uma visualização simples

```python
import matplotlib.pyplot as plt

df['valor'].plot(kind='hist')
plt.show()
```

### 8. Salvar um arquivo novo

```python
df.to_csv('dados_processados.csv', index=False)
```

Esses comandos são a base para boa parte dos exercícios desta pasta.

---

## 🧠 Materiais que agregam à aula

Além do conteúdo principal, estes temas ajudam bastante a consolidar o aprendizado:

- Noções básicas de estatística descritiva
- Visualização de dados com matplotlib e seaborn
- Introdução a SQL para entender bases relacionais
- Leitura de arquivos CSV, Excel e JSON
- Uso de APIs com requests
- Boas práticas de organização de projetos em Python
- Git e GitHub para versionar código e trabalhos

Para estudar mais, vale revisar:

- Conceitos de média, mediana, moda e desvio padrão
- Diferença entre dados qualitativos e quantitativos
- Uso de gráficos: barras, linhas, histogramas e boxplots
- Estruturas básicas de DataFrames e séries

---

## 🧰 Git e terminal

### Instalar Git

#### Windows

1. Baixe em: https://git-scm.com/download/win
2. Instale com as opções padrão
3. Abra o Git Bash ou o terminal do VS Code

#### macOS

```bash
brew install git
```

#### Linux (Ubuntu/Debian)

```bash
sudo apt install git -y
```

### Verificar a instalação

```bash
git --version
```

### Comandos básicos

```bash
git config --global user.name "Seu Nome"
git config --global user.email "seu@email.com"
git status
git pull origin main
git add .
git commit -m "Adiciona material da aula"
git push origin main
```

---

## 🍴 Fork e Pull Request

Se você quiser contribuir com o repositório, o fluxo mais comum é:

1. Fazer um fork no GitHub
2. Clonar o fork localmente
3. Criar uma branch para o trabalho
4. Fazer commits com mudanças claras
5. Enviar para o GitHub
6. Abrir um Pull Request

Exemplo:

```bash
git clone https://github.com/SEU_USUARIO/Harve-School.git
cd Harve-School
git checkout -b aula-4-python-etl-seu-nome
```

---

## ✅ Dica final para o estudo

A melhor forma de aprender com este material é:

- ler o conceito da aula
- rodar os exemplos no terminal ou notebook
- alterar parâmetros e experimentar por conta própria
- registrar dúvidas e soluções em anotações

Se preferir, comece com um exemplo simples e vá evoluindo aos poucos.


5. Por que a média é mais sensível a outliers que a mediana?

6. Se média e mediana são bem diferentes, o que isso indica?

7. Para que serve a média ponderada?

## Separatrizes

1. O que são Q1, Q2 e Q3?

2. Q2 é a mesma coisa que qual outra medida?

3. O que é o IIQ (IQR) e como se calcula?

4. Quais as fórmulas do limite inferior e superior de outlier?

5. O que um boxplot mostra?

6. Outlier é sempre um erro nos dados?

## Dispersão

1. O que a amplitude mede? Qual a fraqueza dela?

2. Qual a diferença entre variância e desvio padrão?

3. Por que o desvio padrão é mais fácil de interpretar que a variância?

4. O que é o coeficiente de variação e por que ele é útil para comparar?

5. Um CV de 40% indica dados previsíveis ou dispersos?

## Python

1. Quais funções calculam média, mediana e moda no pandas?

2. O que `df.describe()` retorna?

3. Para que serve o `df.groupby()`?

4. Qual a diferença entre `.std()` e `.std(ddof=0)`?

---

## Gabarito

**Tipos de dados**

1. Qualitativo descreve uma qualidade ou categoria; quantitativo expressa uma quantidade numérica em que faz sentido somar/subtrair ou medir.

2. Nominal não tem ordem (por exemplo, cor do carro, sabor de sorvete); ordinal tem ordem/escala (por exemplo, tamanho: pequeno, médio, grande).

3. Contínuo pode assumir qualquer valor dentro de um intervalo (por exemplo, altura, peso); discreto tem valores inteiros ou contáveis (por exemplo, número de pessoas, número de vendas).

4. Telefone é qualitativo porque os dígitos são uma etiqueta de identificação, não um valor numérico para operações matemáticas.

5. Variável dummy (dicotômica) é uma variável que só pode assumir dois valores, como 0 e 1, indicando presença/ausência ou sim/não.

6. "Tamanho da casa: pequeno, médio, grande" é um dado ordinal.

**Medidas de posição**

1. A média é a soma dos valores dividida pela quantidade de observações.

2. A mediana é o valor do meio quando os dados estão ordenados; a ordenação é necessária para saber qual valor fica no centro.

3. Quando n é par, a mediana é a média dos dois valores centrais.

4. Moda é o valor que aparece com mais frequência. Sim, pode haver mais de um valor modal ou nenhuma moda.

5. A média usa todos os valores e é afetada por valores extremos; a mediana só depende da posição no conjunto ordenado.

6. Se média e mediana forem bem diferentes, isso indica assimetria na distribuição ou presença de outliers.

7. A média ponderada dá pesos diferentes a cada valor, útil quando nem todas as observações têm a mesma importância.

**Separatrizes**

1. Q1, Q2 e Q3 são os primeiros, segundo e terceiro quartis; dividem os dados em quatro partes iguais.

2. Q2 é a mesma coisa que a mediana.

3. O IIQ (IQR) é a diferença entre Q3 e Q1: IQR = Q3 - Q1.

4. Limite inferior: Q1 - 1,5 × IQR; limite superior: Q3 + 1,5 × IQR.

5. Um boxplot mostra mediana, quartis, faixa interquartílica e possíveis outliers.

6. Não, outlier nem sempre é erro; pode ser um valor raro ou uma variação real que merece investigação.

**Dispersão**

1. Amplitude mede a diferença entre o maior e o menor valor. Sua fraqueza é ser sensível a um único valor extremo.

2. Variância mede a média dos quadrados das distâncias até a média; desvio padrão é a raiz quadrada da variância.

3. Desvio padrão é mais fácil de interpretar porque usa as mesmas unidades dos dados originais.

4. Coeficiente de variação é o desvio padrão dividido pela média; ele compara dispersão relativa entre conjuntos com unidades diferentes.

5. Um CV de 40% indica dados relativamente dispersos e variabilidade alta em relação à média.

**Python**

1. `df['coluna'].mean()`, `df['coluna'].median()`, `df['coluna'].mode()`.

2. `df.describe()` retorna estatísticas descritivas como contagem, média, desvio padrão, valores mínimo/máximo e quartis.

3. `df.groupby()` agrupa dados por uma ou mais colunas para calcular agregações por grupo.

4. `.std()` usa o padrão de amostra (`ddof=1` por padrão); `.std(ddof=0)` calcula o desvio padrão populacional.

---

## Material de Python ETL
A pasta principal para ETL é `Python_ETL`.

### Estrutura principal
- `install.py` — exemplo de banco SQLite local
- `Harve_School_API_application.ipynb` — notebook de aula
- `Harve_School_ETL_first_class.ipynb` — primeiro notebook de ETL
- `FUNCTIONS_DICTIONARY.md` — dicionário de funções usadas nos scripts
- `Aula 3/` — exercícios de manipulação de datas e previsão do tempo
- `Aula 4/` — pipeline ETL completo com CSV e banco de dados

### Principais arquivos em `Aula 4`
- `01_exportando_csv/exportando_csv.py`
- `02_credenciais_bd/credenciais.py`
- `03_lendo_bd/lendo_banco.py`
- `04_escrevendo_bd/escrevendo_banco.py`
- `05_desafio/desafio_final.py`
- `banco/popular_banco.py`

### O que aprender aqui
- Extração de dados de APIs
- Transformação de dados com `pandas`
- Salvamento em `.csv`
- Conexão a bancos com `SQLAlchemy`
- Criação e leitura de tabelas SQLite/MySQL
- Uso de `to_sql`, `read_sql`, `commit()` e `close()`

### Dicas de instalação específicas
```bash
pip install sqlalchemy pymysql python-dotenv
```

### SQLAlchemy rápido
- `create_engine(...)` → cria o motor de conexão
- `engine.connect()` → abre a conexão com o banco
- `text(...)` → cria a query SQL
- `pd.read_sql(query, conn)` → traz o resultado para DataFrame
- `df.to_sql(name, con, if_exists, index=False)` → salva no banco
- `conn.commit()` → confirma a escrita
- `conn.close()` → fecha a conexão

---

## Bibliotecas recomendadas
- pandas: https://pandas.pydata.org/
- matplotlib: https://matplotlib.org/
- seaborn: https://seaborn.pydata.org/
- requests: https://docs.python-requests.org/
- sqlalchemy: https://www.sqlalchemy.org/
- pymysql: https://pymysql.readthedocs.io/
- python-dotenv: https://saurabh-kumar.com/python-dotenv/

---

## Links úteis
- Git: https://git-scm.com/
- GitHub Docs: https://docs.github.com/
- VS Code Source Control: https://code.visualstudio.com/docs/editor/versioncontrol
- Instalar Python: https://www.python.org/downloads/
- SQLAlchemy Docs: https://docs.sqlalchemy.org/
- Pandas Docs: https://pandas.pydata.org/docs/

---

## Dicas finais
- Sempre use `git pull` antes de começar um dia de estudo.
- Mantenha seu ambiente virtual ativado ao trabalhar.
- Se estiver usando o VS Code, prefira o terminal integrado e o painel Source Control.
- Para cada nova aula, crie uma nova pasta `Aula X` e coloque o material lá.
- Documente no commit o que foi alterado, por exemplo: `git commit -m "Adiciona solução do exercício de quartis"`.

Boa jornada de estudos!

