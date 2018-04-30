---
layout: post
title:  "Python - Escondendo entrada do usuário no terminal com a biblioteca Getpass"
date:   2018-04-30 18:16:01 -0600
categories: Python
---

As vezes é comum você querer desenvolver algum script em Python, que vá solicitar que o usuário digite informações sensíveis, como senhas e tokens. O grande problema disso é que, quando o usuário vai inserir essas informações atráves do terminal ou CMD, a mesma, fica totalmente exposta, e isso, por si só é um grande problema de segurança.

Exemplo(No cmd do Windows):

```powershell
Digite seu nome: Victor Lima
Digite sua senha: 1232324343 <-- Ops
```

Então, para resolver este problema, existe no Python, a biblioteca ```getpass``` que serve para esconder as informações digitadas pelo o usuário em algum momento do seu programa, criando o efeito abaixo:

```
Digite seu nome: Victor Lima
Digite sua senha:  <-- O usuário pode digitar a senha aqui, mas ela não vai ser exibida
```

E para usar a Getpass é muito simples, primeiro import ela no ínicio do seu script:

```python
import getpass
```

A classe ```getpass``` tem uma função chamada ```getpass```(Sim, isso mesmo, o mesmo nome da classe), que funciona de uma forma parecida com a função ```input``` , então, por exemplo, se eu quiser receber uma informação, para uma variável ```senha``` ,  basta fazer o que está no exemplo abaixo:

```pyth
senha = getpass.getpass("Digite sua senha ou informação sensível :D : ")
```

Então, após isso, você vai ver que quando a linha de código acima for executada, e quando o usuário for digitar a informação solicitada, esta mesma, vai ser ocultada pela função ```getpass``` .