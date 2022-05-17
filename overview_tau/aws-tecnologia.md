### Tecnologia

Tópicos:
- Definição de métodos de implantação e operação na Nuvem
- Definição da infrastrutura global da AWS
- Identificação dos principais serviços da AWS
- Identificação dos recursos para suporte tecnológico.  

### Como provisionar recursos na nuvem?  
- Acesso programático: SDK e APIs 
- Console Gerenciamento AWS
- CLI
- Interface como Código (YAML e JSON)
- AWS CDK

### Método de implantação na nuvem

- On-premises
- Hybrid Cloud
- Cloud Native

### Infraestrutura Global da AWS

Regiões < Zonas de disponibilidade (datacenters) < edge locations("mini data centers")

- Definições: Regiões é o espaço geográfico em que se agrupam zonas de disponibilidade (availability zones). Os serviços da AWS são separados por região.  
- Availability Zone: Conjunto de data centers que se conectam numa região.  
- Edge Locations: Locais com um pequeno setup para transmitir e cachear os dados (útil para atingir baixa latência). 
	-Ex: o Amazon CloudFront faz uso do Edge para entrega conteúdo com baixa latência. 	Utiliza-se como uma CDN. 
	- AWS Global Accelerator: Ips estáticos como uma única porta de entrada para aplicações 	globais.

#### Alta disponibilidade:  

- Ocorre devido aos serviços estarem distribuídos em mais de uma availability zone  
- Availability Zones não compartilham um únicao ponto de falha.  

#### Utilizar aplicações em multiplas regiões:  
- Para garantir Disaster Recovery.

RPO (Recovery Point Object) - Quantidade de informação que posso perder quando recuperar de uma falha.
RTO (Recovery Time Object) - Quantidade de tempo que o serviço ficará indisponível.  

Níveis de Recuperação para Disaster Recovery:  
- Backup e Restore  
- Pilot Light
- Warm Standby
- Multi-site active/active   

#### Quando utilizar multiplas regiões:  

- Baixa Latência  
- Soberania de dados (Alguns países permitem apenas os dados armazenados dentro do próprio país) 

### Identificação do principais serviços:  

- Computação
- Armazenamento
- Rede
- Banco de Dados







