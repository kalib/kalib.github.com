---
author: kalib
comments: true
date: 2009-03-23 17:35:44+00:00
layout: post
slug: pydev-preparando-o-eclipse-para-o-python
title: Pydev - Preparando o Eclipse para o Python
wordpress_id: 315
categories:
- Arch Linux
- Impressoes
- Linux
- Python
- Software Livre
---

**E**m um mundo onde nem tudo é tela preta, as vezes pode ser cansativo programar sem a ajuda de uma IDE. Para projetos grandes e que possuem uma disponibilidade menor de tempo, estas ferramentas de desesenvolvimento são fundamentais. Aqui gostaria de destacar o Eclipse, que como vocês devem saber não é apenas uma IDE para desenvolvimento Java, em conjunto com o plugin Pydev.

**N**este pequeno passo a passo abordo uma forma simples e direta para se instalar o Pydev transformando seu Eclipse em um ambiente para desenvolvimento em **Python**.

**A**ntes de mais nada, suponho que você já tenha o Eclipse devidamente instalado. Em meu caso, no Arch Linux, instalei através do pacman, portanto estou com a versão 3.4.1, portanto qualquer diferença nos passos seguidos aqui pode ser por diferença em sua versão do Eclipse.

**S**em mais baboseira, vamos ao processo.

**1- **Com seu eclipse rodando, clique na opção Software Updates do menu Help, conforme ilustração:

{% img center /imgs/img01.png 'Python Eclipse' %}

**L**he será exibida uma janela como a seguinte. Selecione a opção Available Software, no canto superior.

{% img center /imgs/img02.png 'Python Eclipse' %}

**2-** Nesta janela de Available Software, clique na opção Add Site. Lhe será apresentada uma janela na qual você deve inserir o endereço <del>https://pydev.sourceforge.net/updates</del> e clica em Ok, como na figura abaixo:

ERRATA: Correção em 2011 -> Novo endereço para atualizações é: [https://pydev.org/updates](https://pydev.org/updates)

{% img center /imgs/img031.png 'Python Eclipse' %}

**3-** Após isto, você terá a opção de instalação do Pydev. Selecione a caixa e clique no botão Install que se encontra no canto superior direito da janela, conforme ilustração.

{% img center /imgs/img04.png 'Python Eclipse' %}

**E**le começará a carregar a instalação e lhe será apresentada uma tela com a licença do plugin. Basta aceitar a licença e seguir em frente.

**A**pós isto, o Eclipse começará a baixar os arquivos necessários e realizará a instalação em si. Após concluída, lhe será pedido para reiniciar o Eclipse para que as alterações tenham efeito. Pode confirmar com Yes.

**C**om isto a instalação já está concluída. Nos resta agora começar um projeto Python. Mãos à obra!

**4-** Com seu Eclipse reiniciado, clique na opção Preferences da aba Window.

{% img center /imgs/img05.png 'Python Eclipse' %}

**5-** Na janela que lhe será apresentada, selecione a aba Pydev e selecione a opção Interpreter - Python. Clicando no botão New, do canto superior Direito, aponte para o caminho onde se encontra seu interpretador Python. (No linux, normalmente será /usr/bin/python.)

{% img center /imgs/img06.png 'Python Eclipse' %}

**L**he será apresentada uma tela como a seguinte. Basta confirmar sem alterações.

{% img center /imgs/img07.png 'Python Eclipse' %}

**R**epare que agora você terá um interpretador Python instalado, bem como uma lista de Paths para o Python em seu sistema. Novamente confirme clicando em Ok, encerrando aqui nossa configuração do Eclipse para programação com Python.

{% img center /imgs/img08.png 'Python Eclipse' %}

**U**ma vez que o plugin Pydev está instalado e devidamente configurado, passamos para o passo final. Teste do Python no Eclipse.

**6****-** Vamos começar criando um novo projeto seguindo o caminho: File > New > Pydev Project.

{% img center /imgs/img09.png 'Python Eclipse' %}

**E**scolha um nome para seu projeto e confirme a criação do mesmo clicando em Finish, conforme imagem a seguir:

{% img center /imgs/img10.png 'Python Eclipse' %}

**U**ma vez que seu projeto foi criado. Ele será listado na barra de projetos localizada no canto esquerdo do Eclipse. Clicando com o botão direito do mouse na pasta src de seu projeto, escolha a opção New > File, conforme ilustração.

{% img center /imgs/img11.png 'Python Eclipse' %}

**C**om seu arquivo em branco, pode fazer seu teste do python com qualquer código simples, como por exemplo o bom e velho "Hello World".

{% img center /imgs/img12.png 'Python Eclipse' %}

**P**ronto pessoal! Agora é só abusar do Python no seu Eclipse.

**A**braços