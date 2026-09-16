Financial Sentiment Analysis: NLP & Word Embeddings

Este projeto é um pipeline completo de Processamento de Linguagem Natural (PLN) voltado para a análise de sentimento de frases do mercado financeiro.

O objetivo principal é extrair textos brutos, realizar uma limpeza rigorosa, vetorizar as palavras utilizando três abordagens diferentes de representação textual (TF-IDF, Word2Vec customizado e GloVe pré-treinado) e preparar os dados para modelagem preditiva.

O script conta com um sistema dinâmico de amostragem controlada via terminal, permitindo testar o fluxo com volumes customizados de dados por classe: neutro, positivo e negativo.

Funcionalidades

Amostragem Customizada: menu interativo via terminal para definir o tamanho da amostra balanceada por classe.

Pipeline de Limpeza Avançado: remoção de tags HTML, conversão para minúsculas, expansão de contrações em inglês, eliminação de caracteres especiais e pontuações e filtragem de ruídos.

Análise Exploratória (EDA): identificação e tratamento automático de valores nulos e registros duplicados.

Geração de Gráficos: exportação automática da distribuição de classes em alta resolução (dpi=300), ideal para apresentações e relatórios acadêmicos.

Engenharia de Recursos (Vetorização):

TF-IDF: extração estatística com limite de até 5000 features.

Word2Vec: treinamento de um modelo semântico customizado e contextualizado com os dados de treino.

GloVe: integração com vetores pré-treinados (glove-wiki-gigaword-100) via API Gensim.

Tecnologias e Bibliotecas

Python (v3.10+)

Pandas & NumPy: manipulação, limpeza e tratamento matricial dos dados.

Scikit-Learn: divisão estratificada de treino/teste (train_test_split), vetorização TF-IDF e métricas de validação.

NLTK (Natural Language Toolkit): tokenização e gerenciamento de stopwords em inglês.

Gensim: criação do modelo Word2Vec e download do modelo GloVe.

Matplotlib: geração e customização de gráficos de barras.

KaggleHub: integração e gerenciamento de datasets hospedados no Kaggle.

Pipeline
Dados Brutos
     ↓
Limpeza e Pré-processamento
     ↓
Análise Exploratória (EDA)
     ↓
Amostragem Balanceada
     ↓
Divisão Treino/Teste
     ↓
Vetorização
 ┌───────┼────────┐
 ↓       ↓        ↓
TF-IDF Word2Vec  GloVe
     ↓
Dados Preparados
     ↓
Modelagem Preditiva

Classes de Sentimento

🟢 Positivo

⚪ Neutro

🔴 Negativo

Autor

Desenvolvido por Assis Vieira e Salomão.
