### Serviços de Banco de Dados    

Na AWS podemos ter o banco de dados configurado dentro do EC2 e também podemos ter serviços gerenciados, no qual a AWS provisiona o banco.  

### RDS (Bancos de dados relacionais [Relational DataBase Services])  

Faz parte dos servios gerenciados, ou seja, a AWS que cuida dele para os usuários.  

Eles possuem a Opção MultiAZ. Quando escolhemos esta opção é feita uma réplica do banco secundário em outra subnet. Se o banco tiver muita leitura e pouca escrita, podemos criar um divisão do tráfego com uma Read Replicas(uma maneira de escalar os banco de dados relacionais para suportar processamento).

[Read Replicas](https://aws.amazon.com/pt/rds/features/read-replicas/). 
*As Réplicas de leitura do Amazon RDS proporcionam desempenho e durabilidade melhores para instâncias de banco de dados (DB) do RDS.*

[Amazon RDS](https://aws.amazon.com/pt/rds/features/)   


* Serviços gerenciados de bancos de dados relacionais  
* Pague pelo que usar  
* PostgreSQL, MySQL, MariaDB, Oracle, SQL Server  
* Amazon Aurora: Próprio da AWS, construído em cima da engine MySQL e PostGreSQL. Promessa que a performance é melhor que os nativos mySQL e postgress.  
*  Aurora Serveless.  Use o banco e após de uma inatividade será pausado.    


### Dynamo DB (Dados não relacionais)

* Banco não relacional gerenciado pela AWS  
* Banco chave valor  
* Tabelas e índices  
* Método de princing: custo por quantidade de escrita e leitura da tabela: RCUs e WCUs.    
* Modo de pagamento: On Demanad ou Provisioned.   

### Amazon Redshift  (Serviço para Big Data)   

* Banco colunar  
* Ideal para data warehouse/ data lake    
* Escalável a peta bytes  
* Totalmente gratuito    


### Suporte aos Serviços  

### Onde procurar conhecimento  
* Documentação: https://docs.aws.amazon.com/pt_br/index.html  
* Knowledge center  
* Whitepapers  
* AWS fórum  
* AWS blogs  

### Suporte AWS  
* Quatro níveis: basic, developer, business, enterprise. 
Descrição para cada plano:  
https://aws.amazon.com/pt/premiumsupport/plans/?nc1=h_ls  

* Central de parceiros AWS   
* AWS Profession Services  
* AWS training   

### AWS Trusted Advisor  
* otimização de custos  
* Performance  
* Segurança  
* Tolerancia a falhas  
* Service limits    

### AWS Personal Health Dashboard (avisos de problemas operacionais)   
* Alertas quando um serviço AWS está fora do ar  
* Criação de alertas que podem afetar a conta  
* Recomendações do que deve ser feito.  
