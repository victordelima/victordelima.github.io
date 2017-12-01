---
layout: post
title:  "Instalando e configurando MongoDB no Windows"
date:   2017-11-29 13:33:36 -0200
categories: MongoDB
---
O Processo de instalação e configuração de um SGDB(Sistema de gerenciamento de banco de dados) como o Mongo, nem sempre é tão fácil no Windows como é no Linux ou em um MacOS. Porém não se preocupe, neste artigo nós vamos simplificar tudo para que você tenha o seu Mongo preparado em seu ambiente de desenvolvimento.

![MongoDB Logo](https://i.imgur.com/4Xlnjvm.png)

### 1° Passo - Baixar o software

O Primeiro passo, é baixar o Mongo, é claro, e para fazer isso basta acessar este link: ['Site oficial do Mongo'](https://www.google.com),  após isso, entre na página de downloads:



!["Tela de download"](/assets/mongo/02.png)

Selecione a opção Community Server, que já é o suficiente para o seu ambiente de desenvolvimento. Após isso, escolha a opção **"Windows Server 2008 R2 64-bit and later, with SSL support x64"** , está versão dá suporte para todos os Windows mais atuais(Windows 7, Server 2008 r2 , Server 2012, 8 , 8.1 e Windows 10), após isso clique em download.

### 2° Passo - Instalação

Esse passo é o mais simples de todos, apenas abra o executável e faça o processo de instalação da forma como você faz com qualquer programa no Windows.

> Next... Next.. Next... Install... Finish
>
> -- Bil Gates

Note que quando você abre o instalador, ele apresenta duas opções de instalação, a Complete e a Custom, a primeira, vai instalar todos os recursos necessários para o MongoDB rodar a outros recursos adicionais, Já a Custom, permite que você personalize a sua instalação, definindo um diretório especifico de instalação ,por exemplo. Porém, escolha a opção Complete, pois é a mais indicada para quem está iniciando e que na maioria dos casos já atende bem as suas necessidades. O Mongo será instalando no diretório

> "C:\Program Files\MongoDB"

### 3° Passo - Adicionando o MongoDB no PATH do Windows.

Quando trabalhamos com SGDBs precisamos constantemente utilizar a linha de comando do sistema operacional para fazer operações com a base de dados durante o desenvolvimento de algum projeto. Porém, no ambiente Windows, o MongoDB, não é auto-configurado na sua ferramenta de linha de comando(no caso, o CMD), e para fazer isso, nós precisamos adiciona-lo na váriavel de ambiente PATH do Windows, que tem como uma de suas funções "linkar" executaveis no Prompt de comando, para quando, por exemplo, você digitar  "mongo", ele abrir o utiliário do Mongo no CMD.

E para fazer isso é muito simples. Abra o menu iniciar, e pequise por "Meu Computador"
