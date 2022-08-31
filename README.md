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