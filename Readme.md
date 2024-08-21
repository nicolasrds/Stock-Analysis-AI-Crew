# Stock Market Analysis Application

Este aplicativo fornece uma análise abrangente do mercado de ações utilizando várias ferramentas e agentes, incluindo Yahoo Finance, Google Generative AI e busca de notícias DuckDuckGo. Ele é construído usando Streamlit para o front-end e CrewAI para gerenciar o processo de análise. O aplicativo permite que os usuários insiram um código de ação, e ele retorna insights detalhados do mercado, incluindo tendências de preços, análise de notícias e um resumo em formato de newsletter.

## Funcionalidades

- **Análise de Preços de Ações**: Recupera preços históricos de ações do Yahoo Finance para o último ano e analisa as tendências (alta, baixa ou lateral).
- **Análise de Notícias de Mercado**: Resume os artigos de notícias recentes relacionados à ação selecionada e atribui uma pontuação de medo/ganância.
- **Geração de Newsletter**: Cria uma newsletter abrangente de 3 parágrafos que inclui um resumo executivo, análise baseada em tendências de preços e notícias, e previsões de tendências futuras.

## Como Funciona

1. **Yahoo Finance Tool**: Recupera os preços históricos das ações para o ticker selecionado.
2. **Google Generative AI (ChatGoogleGenerativeAI)**: Utilizado para gerar análises inteligentes e contextuais.
3. **DuckDuckGo Search Tool**: Coleta artigos de notícias recentes relacionados à ação para avaliar o sentimento do mercado.
4. **Agentes do CrewAI**: Três agentes trabalham juntos para realizar a análise e gerar o resultado final:
   - **Stock Price Analyst**: Analisa as tendências dos preços das ações.
   - **News Analyst**: Resume as notícias do mercado e avalia o sentimento.
   - **Stock Analyst Writer**: Compila a análise final em uma newsletter informativa e convincente.

## Instalação

1. Clone este repositório:
   ```bash
   git clone https://github.com/nicolasrds/Stock-Analysis-AI-Crew.git
   cd Stock-Analysis-AI-Crew
   pip install -r requirements.txt
   ```
2. Configure suas variáveis de ambiente:
  . Crie um arquivo secrets.toml no diretório .streamlit.

  ```bash
    google_api_key = "SUA_CHAVE_API_GOOGLE"
  ```

## USO

1. Execute a aplicação Streamlit:
  ```bash
    streamlit run crewai-stocks.py

  ```
