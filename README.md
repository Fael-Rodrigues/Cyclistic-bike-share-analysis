🚴‍♂️ Estudo de Caso: Otimização de Frota e Estratégias de Conversão na Cyclistic

📝 Introdução

Este projeto faz parte do Certificado Profissional de Análise de Dados do Google. O cenário envolve a Cyclistic, uma empresa de compartilhamento de bicicletas em Chicago. O desafio é entender como os membros anuais e ciclistas casuais utilizam o serviço de forma diferente para fundamentar uma nova estratégia de marketing focada em conversão e eficiência operacional.

🛠️ FERRAMENTAS UTILIZADAS
Linguagem: Python

Bibliotecas: Pandas, Matplotlib, Seaborn

Ambiente: Google Colab / Jupyter Notebook


🎯 Etapa 1: Perguntar (Ask)

O objetivo principal é responder a três perguntas fundamentais para a equipe de marketing e executiva:

1.Como os membros anuais e os ciclistas casuais usam as bicicletas da Cyclistic de forma diferente?

2.Por que os passageiros casuais iriam querer adquirir planos anuais da Cyclistic?

3.Como a Cyclistic pode usar a mídia digital para influenciar os passageiros casuais a se tornarem membros?

Tarefa de Negócio: Maximizar o número de membros anuais através da conversão de usuários casuais, utilizando insights baseados em dados para otimizar a oferta e a operação logística.


📂 Etapa 2: Preparar (Prepare)

Os dados utilizados são dados históricos de trajetos da Cyclistic (dados públicos disponibilizados pela Motivate International Inc.).

•Abrangência: 12 meses de dados (Janeiro a Dezembro de 2022).

•Volume: Mais de 5.6 milhões de registros brutos.

•Privacidade: Dados anonimizados, sem informações pessoais dos usuários.

🛠️ Etapa 3: Processar (Process) - Foco em Engenharia de Dados

Para este projeto, escolhi Python como ferramenta principal de ETL devido ao grande volume de dados. O foco foi criar um pipeline robusto e escalável.

Pipeline de ETL Profissional:
•Consolidação: Unificação de 12 arquivos CSV em um único dataset.

•Limpeza Rigorosa: Remoção de nulos, duplicatas e inconsistências logísticas (viagens ≤ 0 min).

•Tradução e Padronização: Renomeação de colunas para o português e ajuste de tipos de dados.

•Otimização: Conversão de colunas para category, reduzindo o tamanho do arquivo final e acelerando o processamento no Power BI.

Script de Engenharia: cyclistic_etl_pipeline.py

📊 Etapa 4: Analisar (Analyze)

A análise exploratória foi realizada inicialmente em Python para identificar tendências globais e, posteriormente, aprofundada no Power BI.

Insights Principais:

•Padrões de Uso: Membros utilizam as bicicletas predominantemente para commuting (ida e volta ao trabalho), com picos às 08h e 17h.

•Perfil Recreativo: Usuários casuais têm maior volume de viagens nos fins de semana e durações médias 2x superiores às dos membros.

•Logística de Frota: Identificação de estações de alta rotatividade que exigem rebalanceamento frequente de bicicletas.


📈 Etapa 5: Compartilhar (Share) - Business Intelligence

Desenvolvi um dashboard interativo no Power BI para visualizar os KPIs e facilitar a tomada de decisão da equipe executiva.

(Espaço reservado para o print do seu Dashboard Power BI)

Diferenciais Logísticos no Dashboard:

•Taxa de Ocupação por Estação.

•Mapeamento de Fluxos de Origem-Destino.

•Análise de Sazonalidade Mensal e Semanal.

💡 Etapa 6: Agir (Act) - Recomendações

Com base nos dados, as três principais recomendações são:

1.Campanhas de Fim de Semana: Criar planos anuais com benefícios específicos para uso recreativo nos fins de semana.

2.Marketing Digital Segmentado: Focar em usuários que realizam viagens longas e frequentes, destacando a economia do plano anual.

3.Otimização Operacional: Ajustar a logística de reabastecimento de estações próximas a parques e áreas de lazer nos períodos de pico dos usuários casuais.


🛠️ PROCESSAMENTO E LIMPEZA DE DADOS

Nesta etapa, os dados brutos foram transformados em um conjunto de dados estruturado e confiável. As principais técnicas aplicadas foram:

1. PADRONIZAÇÃO E TRADUÇÃO DE CATEGORIAS
   
Os dados originais continham termos em inglês que dificultariam a apresentação final.

Técnica: Utilização do método .map() com dicionários Python para converter tipos de bicicletas e usuários.

Resultado: Dados amigáveis para o público local (Ex: de classic_bike para Bicicleta Clássica).

2. TRATAMENTO DE VALORES AUSENTES (MISSING DATA)

Datasets de mobilidade urbana costumam apresentar falhas em registros de estações.

Técnica: Identificação de nulos com .isnull().sum() e remoção estratégica de linhas com dados incompletos usando .dropna().

Impacto: Garantia de que cálculos de localização e tempo não fossem distorcidos por valores vazios.

3. ENGENHARIA DE ATRIBUTOS (FEATURE ENGINEERING)

Criação de novas variáveis a partir dos dados brutos para extrair insights ocultos.

Cálculo de Duração: Subtração entre ended_at e started_at para obter o tempo total de cada viagem.

Extração Temporal: Uso da função dt.day_name() para isolar o dia da semana e dt.hour para identificar horários de pico.

Conversão de Unidades: Transformação de segundos para minutos para tornar a métrica de duração mais compreensível.

4. FILTRAGEM DE INCONSISTÊNCIAS (DATA AUDIT)

Em dados reais, podem ocorrer erros de sistema (viagens com duração negativa ou testes de manutenção).

Técnica: Aplicação de filtros booleanos para remover viagens com duração inferior a 1 minuto (potenciais erros de travamento) ou viagens com datas inconsistentes.

5. TIPAGEM E ORDENAÇÃO CATEGÓRICA

Garantir que o computador entenda a lógica humana do tempo.

Técnica: Uso de pd.Categorical para definir a ordem cronológica dos dias da semana (Domingo a Sábado).

Resultado: Gráficos ordenados logicamente, evitando a ordem alfabética padrão do Python.

O passo a passo detalhado do desenvolvimento e a execução do código podem ser visualizados diretamente no [Notebook de Análise](Notebooks/projeto_cicle_versao_final.ipynb).
