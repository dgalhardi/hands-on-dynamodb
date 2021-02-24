# O que é o Amazon DynamoDB?

Dentre os inúmeros serviços disponibilizados pela AmazonWS, existe um serviço de banco de dados totalmente gerenciado, ou seja, sem necessidade
de criar infraestrutura para seu uso. Trata-se do Amazon DynamoDB que tem como premissa o desempenho rápido e previsivel com escalabilidade continua. 
Suas vantagens são:
- Não há necessidade de se preocupar com provisionamento, configuração de clusters, drivers e hardware;
- Replicação, aplicação de patches de software ou escalabilidade de clusters;
- Oferece criptografia de repouso, ou seja, elimina a carga e a complexidade  operacionais na proteção de dados confidenciais;
- Pode-se criar tabelas de banco de dados que armazenam e recuperam qualquer quantidade de dados e atendem a todos os níveis de tráfego solicitados;
- É possível aumentar ou diminuir a capacidade de throughput da tabela sem tempo de inatividade ou degradação do desempenho;
- É possível monitorar a utilização de recursos e métricas de desempenho;
- Oferece o recurso de backups completos sob demanda para retenção e arquivamento de longo prazo conforme as necessidades;
- Tem o recurso de recuperação point-in-time das tabelas que ajudam a protege-las de operações acidentais de gravação ou exclusão;
- Com o recurso point-in-time é possível restaurar uma tabela para qualquer ponto durante os últimos 35 dias;
- Permite a exclusão automática dos itens com o vida útil (TTL) expirados em tabelas, de modo a ajudar na redução de uso e custo do armazenamento de dados irrelevantes.
- Tempo de resposta consistente e rápido mesmo com grande quantidade de armazenamento e requisitos de throughput;
- Todos os dados são armazenados em discos de estados sólido (SSD);
- Dados são automáticamente replicados através de várias zonas de disponibilidade em uma região da aws,proporcionando maior durabilidade de dados e 
disponibilidade de integração;
- É possível usar tabelas globais para manter as tabelas do DynamoDB em sincronia em todas as regiões da aws;

Contudo nem tudo são flores. Algumas desvantagens:
- É preciso bom entendimento de como ele funciona pois se usado de maneira errada pode resultar em perda de performance e alto custo para mante-lo;
- É usado o Capacity Unit (CU), que é uma medida utilizada para cobrar pelo serviço de leitura e escrita.
- Curva de aprendizado ingreme para entender o design de tabela única;
- Inflexibilidade de adicionar novos padrões de acesso;
- A dificuldade de exportar as tabelas para análise

# Funcionamento

O DynamoDB utiliza chaves primárias para identificar exclusivamente cada item em uma tabela e índices secundários para fornecer mais flexibilidade de
consulta.
Os componentes básicos do DynamoDB são: Tabelas, itens e atributos.
O diagrama a seguir mostra uma tabela People com alguns itens,sendo que cada item representa uma pessoa e e cada item é composto por um ou mais atributos.

![alt text](https://github.com/diegowsu/hands-on-dynamodb/blob/main/HowItWorksPeople.jpg?raw=true)




