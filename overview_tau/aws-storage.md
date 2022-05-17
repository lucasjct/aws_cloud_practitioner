### Serviços de Armazenamento  


###  S3  

* Armazenamento do tipo Object Storage  
* O arquivo sempre é substituído  
* Ideal para a criação de website estáticos.  

link: https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/Welcome.html

#### S3 - Features

Link: https://docs.aws.amazon.com/pt_br/AmazonS3/latest/userguide/Welcome.html#S3Features   

#### S3 - Storage Class  

S3 - Standart  
s3 - Inteligent Tiering  
S3 - Standart - IA
S3 - One Zone - IA  
S3 - Glacier  
S3 - Glacier Deep Archive

Link:

https://aws.amazon.com/pt/s3/storage-classes/?nc=sn&loc=3  


### Amazon EFS - Elastic file   

* Armazenamento em forma de arquivos compartilhados entre serviço de computação.  Envolve ec2, eqs. lambda.    

### S3 Vs EBS Vs EFS  Armazenamento de blocos, arquivos e objetos.  

Entender a diferença entre estes.

#### Sumário Armazenamento  

* S3 - Tipo Object Storage, sempre substitui(acesso público ou privado)
* Instance Store (Os dados armazenado morrem junto com a finalização da instância)
* EBS - Em blocos  (acesso liberado apenas para comunicação entre recursos de computação )
* EFS - São files que serão compartilhados (acesso liberado apenas para comunicação entre recursos de computação ).

 Casps de uso para os tipos de armazenamento:
 
S3: ARQUIVOS de bigdata,objetos, backpus de arquivos, entrentenimento, mídias, arquivos que sevem ao próprio site, planilhas.
EBS: boot volumes, usar com banco de dados (ssd e hd)
EFS: Compartilhamento e arquivos. Enfáse no compartilhamento (será EFS).
 
 Link: https://aws.amazon.com/pt/products/storage/
 
 ### AWS Storage Gatway (CLoud Híbrida):   
 
 * Conectar on-premises para acessar os dados na nuvem;
 * use case de hybrid cloud  
 * Faz conexão de armazenamento entre on-premises e nuvem.   
 
 
 #### Tipos AWS Storage Gateway:    

 * File Gateway - Acessar backups - armazenamento híbrido, acesso com cache de dados, migração de dado, armazenamento em blocos, Protocolo: SMB/NFS:  
      * s3
      * fsx - File Server  
* Volume Gateway - Armazenamento Híbrido, acesso com cache de dados, migração de dados, armazenamento em bloco, protocolo iSCI 
* Tape Gateway - Criação de backups, legados, arquivos raramente acessados, subistituir fitas físicas, protocolo iSCI.   


