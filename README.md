# Desafio Cientista de Dados - Análise de Filmes (PProductions)

## Descrição do Projeto
Este projeto tem como objetivo principal analisar um banco de dados de filmes do IMDB para ajudar um estúdio de Hollywood chamado PProductions, e agora deve fazer uma análise em cima de um banco de dados cinematográfico para orientar qual tipo de filme deve ser o próximo a ser desenvolvido.

## Como Executar
1.  **Clone o repositório:**
    `git clone https://github.com/seu_usuario/seu_repositorio.git`

2.  **Instale as dependências:**
    Navegue até o diretório do projeto e instale os pacotes necessários usando o arquivo `requirements.txt`.
    `pip install -r requirements.txt`

3.  **Execute o Notebook:**
    Abra o Jupyter Notebook ou JupyterLab e selecione o arquivo `notebook_analise_final.ipynb`. Você pode executar todas as células para reproduzir a análise e ver os resultados.

# Relatório de Análise e Conclusões

## Análise Exploratória e Limpeza (EDA)

A análise inicial revelou que os dados precisavam de limpeza. As colunas **Gross**, **Released_Year** e **Runtime** foram convertidas de texto para o formato numérico correto. Essa etapa foi crucial para permitir as análises subsequentes.

A análise de correlação mostrou que a **nota do IMDB** e o **faturamento de um filme** têm uma forte relação com o **número de votos**. Esse foi o primeiro grande insight do projeto: a popularidade do filme é um fator chave para o sucesso.

## Respostas para as Perguntas-Chave

### 1. Qual filme você recomendaria para um público desconhecido?
**Recomendação:** *The Dark Knight*

Esta resposta foi baseada na **alta nota** e **alta popularidade**. Com uma nota **9.0 no IMDB** e mais de **2,3 milhões de votos**, *The Dark Knight*.

### 2. Quais são os principais fatores que levam ao alto faturamento?
A análise dos filmes mais lucrativos mostrou que o alto faturamento está ligado a:

- **Gêneros:** Filmes de **Ação, Aventura e Sci-Fi** dominam a lista de maiores bilheterias.
- **Reputação do Diretor:** A presença de nomes como **Christopher Nolan** e **James Cameron** indica que a reputação de um diretor é um forte indicador de sucesso financeiro.
- **Popularidade:** Um alto número de votos é um fator consistente entre os filmes mais lucrativos.

### 3. É possível inferir o gênero a partir do resumo do filme?
**Sim, é possível.** A coluna **Overview** é rica em palavras-chave que se alinham com os gêneros oficiais dos filmes. No entanto, a inferência pode não ser perfeita, já que a maioria dos filmes de alta qualidade tem uma trama que se encaixa em múltiplos gêneros.

## Previsão da Nota do IMDB

Para prever a nota de um filme, usaríamos um modelo de regressão. Ele seria treinado com variáveis-chave como **Meta_score**, **No_of_Votes** e o **diretor**, que se mostraram ser os melhores indicadores de nota.

**Previsão para *The Shawshank Redemption*:**

Com base na sua extrema popularidade (maior número de votos no nosso dataset) e na alta nota da crítica, a previsão seria de uma nota acima de **9.0**. A nota alta seria uma consequência direta dos dados que analisamos.
