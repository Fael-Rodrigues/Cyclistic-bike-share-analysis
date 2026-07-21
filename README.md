Estudo de Caso 1: Como um compartilhamento de bicicletas possibilita o sucesso rápido?


📑 SUMÁRIO

•
INTRODUÇÃO

•
CENÁRIO

•
ETAPA 1: PERGUNTAR

•
ETAPA 2: PREPARAR

•
ETAPA 3: PROCESSAR (ENGENHARIA DE DADOS)

•
ETAPA 4: ANALISAR

•
ETAPA 5: COMPARTILHAR (BUSINESS INTELLIGENCE)

•
ETAPA 6: AGIR

•
CONCLUSÃO




<a name="introdução"></a> 📝 INTRODUÇÃO

Este estudo de caso é parte do Certificado Profissional de Análise de Dados do Google. O projeto consiste na análise de dados históricos de uma empresa fictícia de compartilhamento de bicicletas em Chicago, a Cyclistic. O foco é entender o comportamento de diferentes tipos de usuários para fundamentar estratégias de marketing baseadas em dados.

<a name="cenário"></a> 🏢 CENÁRIO

Como analista de dados júnior na equipe de marketing da Cyclistic, recebi a missão de analisar como os membros anuais e os ciclistas casuais usam as bicicletas de forma diferente. O objetivo final é converter ciclistas casuais em membros anuais, pois a equipe financeira concluiu que membros são muito mais lucrativos.




<a name="etapa-1-perguntar"></a> 🎯 ETAPA 1: PERGUNTAR

A pergunta central definida pela diretora de marketing, Lily Moreno, foi:


"Como os membros anuais e os ciclistas casuais usam as bicicletas da Cyclistic de forma diferente?"

TAREFA DE NEGÓCIO

Identificar tendências e padrões de uso para recomendar estratégias de conversão de usuários casuais em membros anuais, aumentando a rentabilidade a longo prazo da empresa.




<a name="etapa-2-preparar"></a> 📂 ETAPA 2: PREPARAR

Os dados foram obtidos através do repositório público da Cyclistic, cobrindo o período de Janeiro a Dezembro de 2022.

•
Fonte: Dados históricos de trajetos da Cyclistic.

•
Formato: 12 arquivos CSV consolidados.

•
Credibilidade: Dados originais e atuais, disponibilizados pela Motivate International Inc. sob licença específica.




<a name="etapa-3-processar"></a> 🛠️ ETAPA 3: PROCESSAR (ENGENHARIA DE DADOS)

Para lidar com o volume massivo de dados (+5.6 milhões de registros), utilizei Python para construir um pipeline de ETL robusto.

FERRAMENTAS UTILIZADAS:

<div style="display: inline_block">

  <img align="center" alt="Python" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/python/python-original.svg">
  <img align="center" alt="Pandas" height="30" width="40" src="https://raw.githubusercontent.com/devicons/devicon/master/icons/pandas/pandas-original.svg">
</div>

LIMPEZA E TRANSFORMAÇÃO:

•
Consolidação: Unificação dos 12 meses em um único DataFrame.

•
Tratamento de Nulos: Remoção estratégica de registros incompletos para garantir a integridade.

•
Engenharia de Dados: Criação de colunas de duração (minutos ), dia da semana e mês.

•
Otimização: Conversão de tipos de dados para category, reduzindo o uso de memória em 40% e acelerando o Power BI.


Acesse o Script de ETL: cyclistic_etl_pipeline.py




<a name="etapa-4-analisar"></a> 📊 ETAPA 4: ANALISAR

A análise exploratória revelou comportamentos distintos e previsíveis:

•
MEMBROS ANUAIS: Utilizam o serviço de forma utilitária, com picos claros nos horários de entrada e saída do trabalho (08h e 17h) durante os dias úteis.

•
CICLISTAS CASUAIS: Demonstram um perfil recreativo, com viagens 2x mais longas e maior volume de uso aos sábados e domingos.




<a name="etapa-5-compartilhar"></a> 📈 ETAPA 5: COMPARTILHAR (BUSINESS INTELLIGENCE)

Desenvolvi um Dashboard interativo no Power BI para apresentar os KPIs de forma executiva.

DESTAQUES DO DASHBOARD:

•Painel 1: Visão Geral com Total de Viagens, Duração Média e Mix de Usuários.

•Painel 2: Análise de Sazonalidade Mensal e Preferência de Ativos (Bicicletas Elétricas vs Clássicas).

•Painel 3: Estratégia de Conversão focada nas Estações de Maior Fluxo Casual.

(Espaço reservado para as imagens do seu Dashboard)




<a name="etapa-6-agir"></a> 💡 ETAPA 6: AGIR

Com base nos insights, propus as seguintes ações:

1.
CAMPANHA "FIM DE SEMANA CYCLISTIC": Oferecer descontos em planos anuais focados no uso recreativo.

2.
MARKETING DIGITAL GEOLOCALIZADO: Focar anúncios nas estações de maior fluxo casual durante os períodos de verão.

3.
CONVERSÃO POR TEMPO: Criar incentivos para usuários que realizam viagens superiores a 20 minutos (perfil típico de casual).




<a name="conclusão"></a> 🏁 CONCLUSÃO

Este projeto demonstrou que, embora os usuários casuais tragam receita imediata, a estabilidade dos membros anuais é a chave para o crescimento. A integração entre Python (Engenharia) e Power BI (Analytics) permitiu uma visão 360º do problema, entregando uma solução baseada em evidências para a equipe executiva.




Rafael Rodrigues
Analista de Dados
LinkedIn | GitHub






Rafael Rodrigues
Analista de Dados
LinkedIn | GitHub



O passo a passo detalhado do desenvolvimento e a execução do código podem ser visualizados diretamente no [Notebook de Análise](Notebooks/projeto_cicle_versao_final.ipynb).
