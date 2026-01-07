🚴‍♂️ ESTUDO DE CASO: ANÁLISE DE DADOS DA CYCLISTIC

📋 SOBRE O PROJETO

Este projeto faz parte do Certificado Profissional de Análise de Dados do Google. O objetivo é analisar os dados históricos de trajetos da empresa fictícia de partilha de bicicletas, Cyclistic, sediada em Chicago. O desafio consiste em identificar como os Membros Anuais e os Ciclistas Casuais utilizam as bicicletas de forma diferente para orientar uma nova estratégia de marketing.

🛠️ FERRAMENTAS UTILIZADAS
Linguagem: Python

Bibliotecas: Pandas, Matplotlib, Seaborn

Ambiente: Google Colab / Jupyter Notebook

PERGUNTAS DE NEGOCIO

Como os membros anuais e os ciclistas casuais usam as bicicletas da Cyclist de maneira diferente?

Por que os usuários casuais iriam querer adquirir planos anuais da Cyclist?

Como a Cyclist pode usar a mídia digital para influenciar os usuários casuais a se tornarem membros?

⚙️ PROCESSO DE ANÁLISE (METODOLOGIA)

O projeto foi estruturado seguindo as seis etapas do processo de análise de dados:

1. PERGUNTAR (ASK)
   
O objetivo principal é entender como os membros anuais e os ciclistas casuais usam as bicicletas de forma diferente.

Problema de Negócio: Como converter usuários casuais em membros anuais?

Principais Interessados: Lily Moreno (Diretora de Marketing) e equipe executiva da Cyclistic.

2. PREPARAR (PREPARE)
   
Os dados foram obtidos de fontes primárias da Cyclistic (dados públicos).

Armazenamento: Os dados originais foram organizados em arquivos CSV.

Verificação: Identificamos as colunas de tempo (início e fim da viagem), localização das estações e tipos de usuários.

3. PROCESSAR (PROCESS)

Utilizei Python para garantir a escalabilidade e a reprodutibilidade da limpeza.

Limpeza de Dados: Remoção de duplicatas e tratamento de valores ausentes (NaN).

Engenharia de Dados: Criação das colunas duracao_viagem(min) e dia_semana.

Tradução: Padronização das categorias para o português (Ex: classic_bike para Bicicleta Clássica).

4. ANALISAR (ANALYZE)

Nesta etapa, os dados foram agregados e resumidos.

Cálculos: Realização de médias, contagens e agrupamentos por tipo_usuario.

Identificação de Tendências: Cruzamento entre volume de viagens e dias da semana para encontrar padrões de comportamento.

5. COMPARTILHAR (SHARE)

A visualização foi feita com Matplotlib e Seaborn, focando em clareza para stakeholders não técnicos.

Foco: Gráficos que comparam diretamente as métricas entre os dois grupos de usuários.

📂 ORIGEM E LICENÇA DOS DADOS

Os dados utilizados nesta análise são reais e referem-se ao histórico de viagens da Cyclistic, operada pela Motivate International Inc.

Fonte dos Dados Brutos: Os arquivos utilizados foram obtidos diretamente do servidor de armazenamento da empresa: Cyclistic Trip Data Index.

Licença de Uso: Os dados foram disponibilizados sob o Acordo de Licença de Dados da Divvy/Cyclistic, que permite a análise, processamento e exibição das informações para fins de estudo de caso.

Privacidade e Ética: De acordo com as normas de proteção de dados, todas as informações de identificação pessoal (PII) dos ciclistas, como nomes, números de cartão de crédito ou endereços residenciais, foram removidas ou omitidas na fonte para garantir a privacidade dos usuários.

Acessibilidade: Uso de cores distintas e rótulos de dados (labels) para facilitar a interpretação.

6. AGIR (ACT)

Conclusão baseada nos insights para apoiar a tomada de decisão.

Ações Sugeridas: Campanhas de marketing direcionadas para o público casual no verão e foco na economia do plano anual para viagens longas.

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
