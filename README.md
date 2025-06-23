# Análise de Campanha de Cupons - iFood

![img-logo](static/IFood_logo.png)

Este repositório contém a solução completa para um case técnico de Data Analyst, focado em avaliar o impacto de uma campanha de cupons do iFood por meio de uma análise de teste A/B. O objetivo é transformar dados em insights acionáveis, analisar a viabilidade financeira da campanha e propor um plano de ação estratégico para otimizar futuras iniciativas de crescimento.

A análise aprofundada, as conclusões e as recomendações estratégicas para as lideranças de negócio estão consolidadas no relatório final: **[Case_Ifood_DA.pdf](Case_Ifood_DA.pdf)**.

## 📂 Estrutura do Repositório

O projeto está organizado da seguinte forma para garantir a reprodutibilidade da análise:

```
.
├── static/
├── 0_download_data.ipynb
├── 1_process_data.ipynb
├── 2_EDA.ipynb
├── 3_campain_analysis.ipynb
├── Case_Ifood_DA.pdf
├── README.md
└── requirements.txt
```

-   **`static/`**: Contém imagens e outros arquivos estáticos utilizados nos notebooks.
-   **`Notebooks (*.ipynb)`**: Sequência de notebooks Jupyter com o código Python e PySpark para a execução da análise.
-   **`Case_Ifood_DA.pdf`**: Relatório final em PDF com a análise completa, destinado a uma audiência de negócio.
-   **`requirements.txt`**: Lista de dependências Python para o projeto.
-   **`README.md`**: Este arquivo de instruções.

## ⚙️ Como Executar o Projeto Localmente

Para replicar a análise e executar os notebooks em seu ambiente local, siga os passos abaixo.

### 1. Pré-requisitos

-   **Python 3.8+**
-   **Java 8 ou 11**: O PySpark depende de uma instalação Java para funcionar.
-   **Apache Spark**: A biblioteca PySpark é uma interface para o Apache Spark.

### 2. Configuração do Ambiente

#### Passo 1: Clone o Repositório

```bash
git clone <URL_DO_SEU_REPOSITORIO>
cd <NOME_DO_SEU_REPOSITORIO>
```

#### Passo 2: Crie um Ambiente Virtual (Recomendado)

É uma boa prática criar um ambiente virtual para isolar as dependências do projeto.

```bash
# Para MacOS/Linux
python3 -m venv venv
source venv/bin/activate

# Para Windows
python -m venv venv
.\venv\Scripts\activate
```

#### Passo 3: Instale as Dependências Python

Instale todas as bibliotecas necessárias listadas no arquivo `requirements.txt`.

```bash
pip install -r requirements.txt
```

#### Passo 4: Configure o PySpark

A configuração do PySpark em um ambiente local pode ser complexa, pois requer que o Apache Spark e o Java estejam corretamente instalados e que as variáveis de ambiente (`SPARK_HOME` e `JAVA_HOME`) estejam bem definidas.

Em vez de detalhar todos os passos aqui, recomendamos fortemente que você siga um guia detalhado e atualizado. O tutorial abaixo é uma excelente referência para configurar o ambiente completo, mas a lógica é similar para diferentes sistemas operacionais:

➡️ **Tutorial Sugerido:** [Guia de Instalação do PySpark no Windows](https://medium.com/@deepaksrawat1906/a-step-by-step-guide-to-installing-pyspark-on-windows-3589f0139a30/)

➡️ **Tutorial Sugerido:** [Guia de Instalação do PySpark no WSL](https://medium.com/@salssouza/how-to-install-pyspark-in-wsl-3c4ac0e7f672)

### 3. Execução dos Notebooks

Os notebooks foram projetados para serem executados em uma sequência específica para garantir que os dados sejam baixados, processados e analisados corretamente. Execute-os na seguinte ordem:

1.  **`0_download_data.ipynb`**
    -   **Objetivo:** Realiza o download dos datasets brutos (JSON, CSV) a partir das URLs fornecidas no case e os armazena localmente.

2.  **`1_process_data.ipynb`**
    -   **Objetivo:** Executa o processo de ETL (Extração, Transformação e Carga). Carrega os dados brutos, realiza a limpeza, transformação e união das fontes, salvando um dataset consolidado e pronto para análise.

3.  **`2_EDA.ipynb`**
    -   **Objetivo:** Conduz uma Análise Exploratória de Dados (EDA) para entender as características da base de clientes e os padrões de pedidos, fornecendo um contexto crucial para a avaliação do teste A/B.

4.  **`3_campain_analysis.ipynb`**
    -   **Objetivo:** Realiza a análise do teste A/B, calculando os indicadores de sucesso, aplicando testes estatísticos de significância, segmentando os clientes e gerando os insights que embasam as conclusões do projeto.

