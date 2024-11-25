# PF_techacker

Sobre a aplicação:

A aplicação consiste em um sistema de chat personalizado, onde você pode se cadastrar, subir documentos PDFs e fazer perguntas acerca deles. A aplicação foi desenvolvida utilizando streamlit, com Pinecone de VectorStore, OpenAI para a geração de respostas e AWS DynamoDB para o armazenamento de usuários e mensagens.

A aplicação está disponível em: [Prod](http://3.15.10.126:8501/)

E o código fonte está disponível em:

[Repo](https://github.com/talesitf/cautious-enigma)

O repositório acima é responsável por fazer o CI/CD da aplicação, utilizando GitHub Actions.

Para rodar a aplicação localmente, basta clonar o repositório e rodar o comando:

```bash
streamlit run app.py
```

Com atenção para as dependências do projeto, que estão no arquivo `requirements.txt` e as variáveis de ambiente necessárias para utilizar os serviços externos.

## CloudFormation

Os arquivos na pasta `CloudFormation` são responsáveis por criar a infraestrutura necessária para rodar a aplicação. Para rodar o CloudFormation, basta rodar o comando:

```bash
aws cloudformation create-stack --stack-name <stack-name> --template-body <file://template-file> --parameters ParameterKey=KeyName,ParameterValue=<Key de acesso para EC2> ParameterKey=InstanceType,ParameterValue=<Instance Type> ParameterKey=OpenAIAPIKey,ParameterValue=<OpenAI APIKey> ParameterKey=PineconeAPIKey,ParameterValue=<Pinecone APIKey>
```

## Relatórios

Além desse Readme, existem mais relatórios disponíveis na pasta `relatórios`, que são responsáveis por documentar o desenvolvimento e testes de segurança da aplicação.

## Autores

- Tales Ivalque Taveira de Freitas