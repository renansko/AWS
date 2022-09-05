# AWS 

client <-> network <-> server

### Server 
- **Compute**: Compute 
- **Memory**: RAM 
- **Storage**: Data 
- **DataBase**: Storage 
- **Network**: DNS, (...) 

## soluçao nuvem
Utilizar o que você precisa quando você precisa, pagando o somente o uso dos recursos que estão sendo utilizados.

## tipos de "nuvens"
- Privada
    - maior segurança para aplicações sensíveis  
    - Utilizado para empresas unicas sem exposição a rede publica
- publica
    - Recursos de nuvens provisionadas por uma terceira empresa
    - autoatendimento
    - escabilidade e elasticidade 
    - Sem custo de hardware então existe somente o custo operacional OPEX
- hibrida
    - Recursos locais e na nuvem
    - controle de sua infraestrutura local
    - custo e acessibilidade de uma nuvem publica

___

### **IaaS** Infrastructure as a Service

1. blocos de construção "recursos" para o T.I em nuvem
2. provendo: Network, CPU, data storage space
3. Flexibilidade, T.I tradicional para nuvem.

### Exemplos:
- Amazon EC2
- GCP, Azure, Rackspace, Digital Ocean, Linode

### **PaaS** Platform as a Service

1. Necessidade de ter a infraestrutura local,
2. Foco em implementar e manejar suas aplicações

### Exemplos:
- Elastic Beanstalk (on AWS)
- Heroku, Google App Engine (GCP), Windows Azure (Microsoft)

### **SaaS** Software as a Service
1. Produto completo rodando por um provedor (I.A).


### Exemplos:
- Many AWS services (ex: Rekognition for Machine Learning)
- Google Apps (GMAIL), Dropbox, Zoom

____
### **AWS Region**
- Temos regioes aws por todo o mundo.
- A região é um local de data centers

__como escolher uma região:__
- **Comformidade** com o governo as vezes o seu dado ou o produto não deve sair daquela determinada região.
- Latência
- Serviços habilidados, algumas regioes são limitadas nos Serviços
- Preços variam entre regiões

__Availability Zone:__
No minimo duas e no maximo 6.
Cada zona de acessibilidade não dependendem uma da outra.

___

# IAM
- Conta root é criada automaticamente
- Usuarios são pessoas de sua organização que podem ser agrupadas 
- Grupo pode ter somente pessoas
- Usuarios não precisam pertencer a um grupo, e pode pertencer a varios grupos

**JSON document** ``-> `` JSON que contem atribuição de permissões para um determinado Recurso (no caso IAM). 

___segurança__ é uma boa pratica criar um novo usuario com a permissão de adm igual ao root, realizar o login nela e realizar suas implantações por ela_

OBS: tipo de credencial:
 - Senha: acesso ao Console de Gerenciamento da AWS

![Imagem url para login novo IAM](/img/URL_conta_adm.jpeg)

### IAM Policy
- politica em nivel de grupo-
- politica de operação
- policita inline
- Structure:

``"Version": versão da politica``

``"ID": Idendificador para a politica ``

    "Statement": { 
    "Sid": idendificador para o Statement
    "Effect": qual o efeito essa politica vai permitir, "allow ou deny"
    "Principal": "Account/user/role" de qual recurso essa politica vai ser aplicada
    "Action": lista de ações que essa politica vai conseguir realizar
    Resources: Lista de recursos que ações seram aplicadas
    Condition: Condições para a politica

### IAM role

- Dar permissões para serviços na AWS, alguns serviços necessitão de permissão para executar algumas determinadas tarefas.

# EC2

Elastic Compute Cloud

### EC2 User Data

Bootstrapping é um script realizada na criação da sua instancia, para automatizar algumas tarefas.

Uma instancia ec2 ao ser encerrada pode alterar seu IPV4 publico mas não o privado

### Tipos de EC2

- aws.amazon.com/ec2/instance-types/

instances.vantage.sh #Compara instancias

m5.2xlarge

m = classe da instancia

5 = geração

2xlarge = tamanho da instancia

 