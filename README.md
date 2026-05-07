# [Criação de uma aplicação web de três camadas com ASP.NET 2.0, C#, Spring.Net e NHibernate (2010)](https://stahe.github.io/pt-pam-aspnet-juin-2010/)

Este documento apresenta o desenvolvimento passo a passo do **SimuPaie**, uma aplicação .NET concebida para simular o cálculo da remuneração de cuidadores infantis. A abordagem é dupla: **estabelecer uma arquitetura de software clara** e **implementar a solução utilizando as tecnologias .NET disponíveis na altura**. Mais concretamente, o documento descreve uma **arquitetura de três camadas** composta por uma camada de acesso aos dados (DAO), uma camada de negócio e uma camada de apresentação, todas elas integradas através do **Spring IoC**.

## Objetivos do curso

O objetivo deste caso prático é demonstrar como projetar uma aplicação web fácil de manter através de uma separação clara de responsabilidades:

- **Camada 1 - DAO**: acesso aos dados armazenados na base de dados.
- **Camada 2 - Negócio**: cálculos de salários e regras de negócio.
- **Camada 3 - IU**: interação com o utilizador e visualização de resultados.
- **Integração** das camadas através de **interfaces .NET** e **injeção de dependências com Spring IoC**.

O documento também descreve o ciclo de processamento dos pedidos dos utilizadores: a aplicação recebe o pedido, reencaminha-o, se necessário, para a camada de negócio e, em seguida, para a camada de acesso aos dados, antes de enviar uma resposta adequada ao cliente.

## Versões sucessivas da aplicação

A documentação não se limita a uma única implementação. Apresenta várias variantes do SimuPaie para ilustrar diferentes abordagens arquitetónicas e de interface:

1. uma versão **ASP.NET de formulário único** com uma arquitetura de nível único;
2. uma versão equivalente melhorada com **Ajax**;
3. uma versão **ASP.NET de três camadas** com **NHibernate** para o acesso aos dados;
4. uma versão **de página única com múltiplas vistas**;
5. uma versão orientada para **serviços web** do lado do servidor;
6. uma versão cliente ASP.NET que consome este serviço;
7. uma versão **multivista e multipágina**;
8. uma versão cliente do serviço web;
9. uma variante de três camadas que se baseia em maior medida em classes do Spring para facilitar a utilização do NHibernate;
10. uma versão cliente **FLEX**.

## Pré-requisitos

Este documento destina-se a um nível **intermédio**. Presume-se um conhecimento básico de:
- **ASP.NET**
- **C# 2008**: classes, interfaces, herança, polimorfismo
- **Spring IoC / injeção de dependências**
- **arquitetura web de três camadas** e o modelo **MVC**.

## Ferramentas e tecnologias abordadas

O caso prático baseia-se num conjunto coerente de ferramentas e frameworks:

- **Visual C# 2008**
- **Visual Web Developer Express 2008**
- **SQL Server Express 2005**
- **Spring.Net / Spring IoC**
- **NHibernate**
- **NUnit** para testes unitários.

## O que este repositório oferece

Este recurso será de especial interesse para os leitores que desejem:

- compreender a implementação de uma **arquitetura de n camadas** num ambiente .NET;
- ver como **desacoplar** as camadas de apresentação, lógica de negócio e acesso a dados;
- descobrir como utilizar o **Spring.Net** para a montagem de componentes;
- estudar a integração do **NHibernate** numa aplicação web ASP.NET;
- seguir um percurso de aprendizagem passo a passo que avança de uma versão simples para versões mais preparadas para produção.

## Conteúdo do curso

O documento descreve a arquitetura geral da aplicação e, desde a primeira página, utiliza um diagrama para ilustrar as funções do utilizador, da aplicação, das três camadas e do Spring IoC na coordenação de todo o sistema. Por conseguinte, serve tanto como **curso de arquitetura**, **guia de design** e **base de trabalho para a implementação prática**.

Serge Tahé, junho de 2010