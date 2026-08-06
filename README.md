## AWS-S3-Static-Website-Hosting-Lab

<p align="center">

  <img src="https://img.shields.io/badge/AWS-Cloud-orange?logo=amazonaws">

  <img src="https://img.shields.io/badge/Amazon-S3-red?logo=amazons3">

  <img src="https://img.shields.io/badge/AWS_CLI-Terminal-232F3E?logo=amazonaws">

  <img src="https://img.shields.io/badge/Linux-Ubuntu-E95420?logo=ubuntu">

  <img src="https://img.shields.io/badge/HTML5-E34F26?logo=html5">

</p>


<p align="center">
  <img src="capa-lab.png" alt="AWS S3 Static Website Hosting Lab" width="650">
</p>



## Visão Geral

Este projeto apresenta a implementação prática de uma solução de Static Website Hosting utilizando Amazon S3, demonstrando o processo completo desde a criação do bucket até a disponibilização pública de uma aplicação web estática.

O laboratório foi executado utilizando principalmente AWS CLI, simulando uma abordagem utilizada por profissionais de Cloud para gerenciamento e automação de recursos AWS.

Durante a implementação foram explorados conceitos fundamentais:

Object Storage
Controle de acesso
Bucket Policy
Segurança AWS
Publicação de conteúdo estático
Gerenciamento via linha de comando


### Arquitetura da Solução

<p align="center">
  <img src="arquitetura-solucao.png" alt="Arquitetura da Solução" width="650">
</p>

Fluxo da arquitetura:

Usuário
   |
   | HTTPS
   |
Navegador Web
   |
   |
Amazon S3 Static Website Hosting
   |
   |
Bucket S3
   |
   |
index.html

O usuário realiza uma requisição HTTPS para o endpoint público do Amazon S3.

O serviço S3 processa a solicitação e entrega o conteúdo estático armazenado no bucket.


### Objetivos do Projeto

Criar e configurar um bucket Amazon S3
Utilizar AWS CLI para gerenciamento de recursos
Realizar upload de objetos
Configurar permissões públicas controladas
Implementar Bucket Policy
Habilitar hospedagem de website estático
Validar publicação através de navegador
Aplicar conceitos de segurança AWS


## Serviços AWS Utilizados

Amazon S3	Armazenamento e hospedagem do website
AWS CLI	Gerenciamento via terminal
IAM	Controle de identidade e acesso
EC2 Instance Connect	Ambiente Linux para execução dos comandos

 
 ### Implementação
 
 1.Configuração da AWS CLI

Inicialização das credenciais temporárias:

aws configure

Configurações utilizadas:

AWS Access Key
AWS Secret Access Key
Region: us-west-2
Output Format: json


2.Criação do Bucket S3
aws s3 mb s3://eliana-diniz-lab-s3-20260805

Resultado:
make_bucket: eliana-diniz-lab-s3-20260805


3.Upload do Website

Arquivo utilizado:

index.html

Comando:

aws s3 cp index.html s3://eliana-diniz-lab-s3-20260805

Resultado:
upload: ./index.html


### Configuração de Segurança

Inicialmente, o acesso público foi bloqueado pelo mecanismo: 
Amazon S3 Block Public Access
Ao tentar acessar o arquivo:
Resultado:
Access Denied

Esse comportamento demonstrou a proteção padrão aplicada pelo Amazon S3.
Foram realizadas as seguintes configurações:

Revisão do Block Public Access
Criação de Bucket Policy
Permissão de leitura pública controlada
Validação do acesso externo


## Resultado Final

Após as configurações:

Website publicado com sucesso
Arquivo HTML acessível via navegador
Conteúdo hospedado diretamente no Amazon S3

Aplicação publicada:
Mom & Pop Café


### Troubleshooting Realizado

Durante o laboratório foram analisados problemas relacionados a:

Permissões de acesso
Bloqueio de acesso público
Configuração de políticas S3
Validação do endpoint

A resolução envolveu análise de configurações de segurança e ajustes de permissões seguindo as boas práticas AWS.

### Conhecimentos Desenvolvidos

Este projeto permitiu consolidar conhecimentos em:

Cloud Computing
Amazon S3
AWS CLI
IAM
Segurança em Nuvem
Static Website Hosting
Object Storage
Troubleshooting AWS


### Sobre a Autora

Eliana Diniz

Cloud Computing | AWS | Data Analytics | IA Generativa | Machine Learning

Profissional em transição para Cloud, desenvolvendo projetos práticos utilizando serviços AWS, automação via CLI e soluções baseadas em dados e inteligência artificial.

Meu objetivo é transformar conhecimento técnico em soluções reais, aplicando boas práticas de arquitetura, segurança e eficiência operacional.

Linkedin: www.linkedin.com/in/eliana-diniz
