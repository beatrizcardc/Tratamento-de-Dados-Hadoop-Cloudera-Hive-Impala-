# Challenge FIAP - AWSDataQuality - Banco PAN

INTRODUÇÃO
1 Hands On – Transformação de dados semiestruturados em estruturados
1.1 Contextualização

Dados de fluxo contínuo com rastros de navegação web são valiosos para análise da audiência dos sites. Pode-se, por exemplo, criar uma correlação entre as visualizações de produtos e as conversões em vendas efetivamente. Analisar a origem do clique, encontrar as sazonalidades de acesso, entre outros KPIs possíveis.

O grande desafio nesse caso é tornar inteligível (tabular) esses logs capturados via web. Esse, portanto, será o nosso trabalho nesse hands on.

1.2 Orientações Gerais

Você deverá utilizar a VM Cloudera disponibilizada no seguinte endereço: <>

Nela, deve encontrar o arquivo de log de um e-commerce disponível em:

1.3 Sugestão de Road Map

·         Crie no HDFS, dentro de /user/hive/warehouse um diretório “log” para receber o arquivo;

·         Faça a ingestão do arquivo de log para o diretório criado. Você pode fazer a carga do dado via Bulk Upload pelo terminal, ou ainda utilizar ferramentas de ingestão, tais como Flume ou Nifi;

·         Crie uma tabela dentro do editor Hive a partir do log e aplique expressão regular para tabular os dados (veja o tópico de dicas);

·         Sumarize os dados, filtrando apenas os cliques cujo usuário foi até o nível de produto na URL e conte o total de visualizações. Faça a sumarização no Impala. 

Importante: no nome do diretório log, acrescente o seu número de RM. Exemplo: /user/hive/warehouse/log_rmxxxxxx

Sempre que criar uma tabela, o nome deverá ser nomedatabela_rmxxxxxx.

Mantenha esse padrão na criação de objetos de forma geral: tabelas, arquivos, diretórios, scripts.

Como evidência da realização do Hands On, capture as telas de cada etapa do exercício, monte um arquivo em Word com o passo a passo, envie também o script utilizado no Hive e no Impala.

1.4 Bônus

Você pode baixar esses dados em um arquivo de texto e gerar saídas analíticas em uma ferramenta de Data Discovery, tal como Tableau, Qlik View, Power BI, ou mesmo criar os gráficos no Excel.

