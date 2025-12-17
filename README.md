# Cloud News Analyzer

Cloud News Analyzer è una web application cloud-native che raccoglie,
analizza e visualizza notizie online utilizzando servizi AWS.

## Architettura
Il sistema è basato su un'architettura serverless e container-based.
L'ingestione delle notizie è gestita da un container Docker eseguito
su Amazon ECS Fargate e schedulato tramite Amazon EventBridge.
I dati grezzi vengono salvati su Amazon S3 e successivamente elaborati
da funzioni AWS Lambda, che utilizzano Amazon Comprehend per
l'analisi del sentiment e salvano i risultati su Amazon DynamoDB.

L'accesso ai dati avviene tramite API REST esposte da Amazon API Gateway
e implementate con AWS Lambda.
Il frontend è una web application statica sviluppata in React,
ospitata su Amazon S3 e distribuita tramite Amazon CloudFront.

## DevOps
L'infrastruttura è definita tramite Infrastructure as Code
utilizzando AWS CloudFormation.
Il processo di build e deploy del container è automatizzato
tramite AWS CodePipeline e AWS CodeBuild.
Il progetto è sviluppato utilizzando un account AWS Academy.

## Tecnologie
- Amazon ECS Fargate
- AWS Lambda
- Amazon S3
- Amazon DynamoDB
- Amazon API Gateway
- Amazon CloudFront
- Amazon EventBridge
- AWS CodePipeline & CodeBuild
- AWS CloudFormation

