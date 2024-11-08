# ArquiteturaServerless
Arquitetura Serverless AWS

    Hoje compartilho feliz minha primeira Arquitetura AWS, que foi elaborada em conjunto com os colegas Rafael Silva Willians e Wagner Lopes no último final de semana. 
     No início, quando fui mexer no draw.io tomei uma coça kkkk, recebi algumas informações dos colegas, fiz algumas pesquisas, pratiquei bastante e consegui concluir esta manhã o projeto no qual havíamos definido. 
     Nós conversamos sobre projetos diferentes e decidimos pelo desenvolvimento de uma Arquitetura Serverless pequena, simulando a um caso de uso de um cliente que hospedaria seu site na AWS.
     O objetivo era garantir que o conteúdo fosse distribuído com rapidez e eficiência para usuários finais, independente de sua localização geográfica. 
     Além disso, a arquitetura / infraestrutura oferece segurança a acessos não autorizados e distribuição global do conteúdo. 


==> Fluxo da Arquitetura:
 
Usuário -> Acessa o site ou aplicativo, este acesso começa pelo domínio da aplicação, gerenciado pelo Route 53 e direcionando ao CloudFront.

 Route 53 e CloudFront -> direciona a solicitação para o servidor mais próximo e entrega o conteúdo rapidamente.

AWS WAF e Certificado SSL -> verifica segurança da solicitação e estabelece conexão HTTPS segura.

API Gateway -> recebe e direciona a solicitação do usuário e levará a um Lambda 

Lambda -> Processa a lógica da aplicação sem servidor 
              -> Acessa DynamoDB (dados NoSQL) ou S3 (arquivos) ou Aurora Serverless (dados relacionais) conforme necessário .. 

VPC com sub-rede privada -> Protege dados sensíveis. (Lambda e Aurora Serverless)

CloudWatch e CloudTrail -> monitora e registra atividades.

Secrets Manager -> armazena senhas e credenciais de forma segura.

EventBridge -> dispara ações automáticas p/ eventos específicos.

Systems Manager -> gerencia e automatiza a infraestrutura

----------------------------------------------------------------------------------

      Foi uma experiência incrível de aprendizado e, apesar de ser um projeto simples, fiquei empolgada em ter trabalhado em Equipe com os colegas que foram muito pacientes kkk.

      
#AWS #ArquiteturaServerless #Site #TrabalhoemEquipe #Gratidão


Arquitetura original pode ser acessada em meu LinkedIn, no link abaixo:

https://www.linkedin.com/posts/patricia--sousa_aws-arquiteturaserverless-site-activity-7259638865794154497-ZCDC?utm_source=share&utm_medium=member_android
