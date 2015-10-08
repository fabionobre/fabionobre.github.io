---
layout: post
title:  "O que esperar ao modificar o ip do servidor"
date:   2015-10-08 07:10:00
categories: internet
tags: featured
image: /assets/photos/internet.jpg
---
#Começando do começo, o que é DNS ?

Sendo bem simplista, DNS é um conjunto de computadores que tem a função de traduzir um endereço textual para um endereço IP. Assim, quando você quer acessar um site e digita o endereço www.qualquersite.com.br o seu browser irá acessar a rede de servidores DNS e encaminhar a requisição para o servidor correto.

Quando se faz uma alteração no endereço IP de um DNS, estamos dizendo que agora ao acessar um site X, o servidor DNS deverá encaminhar a requisição para outro endereço IP.

Vendo de fora parece algo simples e rápido de ser feito. Porém a rede DNS é formada por vários níveis de hierarquia com vários computadores. E para que todos os computadores possam estar com o novo endereço atualizado demora tempo.

O registro.br afirma que publica as alterações de DNS a cada hora e que todo o processo poderá levar até 36 horas para ser concluído.

#O que acontece na prática.

Quando é feita a alteração do endereço DNS os servidores começam a informar (propagar) aos outros servidores que houve uma mudança. E esse ciclo de notificação entre servidores ocorre até que todos estejam atualizados.

Nesse meio tempo, teremos alguns acesso que responderão ao IP antigo e outros que responderão ao IP novo. O que querendo ou não vai ocasionar uma boa bagunça no seu serviço. 

Se além de modificar o servidor você estiver modificando o core da aplicação, a bagunça será maior ainda. Alguns recursos serão solicitados em um servidor, outros serão solicitados em outro gerando falhas e inconsistência.

Foi assim que aconteceu com o Eu Que Faço, tivemos um período de aproximadamente 12 horas de muita instabilidade e inconsistência. Quanto tínhamos dois servidores diferentes respondendo a requisições tanto do serviço novo como do serviço antigo. Felizmente o processo todo não demorou mais de 24 horas.

#Dicas

- Faça a alteração em dias de poucos acessos
- Não modifique serviço e servidor de uma só vez
- Faça com que os dois servidores acessem o mesmo banco de dados durante a mudança
- Avise com muita antecedência aos seus usuário
- Tenha paciência e muita calma

