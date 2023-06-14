
# Proxy em Java

O Proxy é um padrão de projeto estrutural que fornece um objeto que atua como um substituto para um objeto de serviço real usado por um cliente. Um proxy recebe solicitações do cliente, realiza algumas tarefas (controle de acesso, armazenamento em cache, etc.) e passa a solicitação para um objeto de serviço.

O objeto proxy tem a mesma interface que um serviço, tornando-o intercambiável com um objeto real ao ser passado para um cliente.

## Complexidade: ⭐⭐☆

O padrão Proxy em Java tem uma complexidade moderada. Embora a implementação do proxy possa exigir algum trabalho adicional, a estrutura geral do padrão é relativamente direta.

## Popularidade: ⭐☆☆

O padrão Proxy não é amplamente utilizado na maioria das aplicações Java. No entanto, ele ainda é útil em casos especiais onde é necessário adicionar comportamentos extras a um objeto existente sem alterar o código do cliente.

## Exemplos de uso:

Embora o padrão Proxy não seja amplamente utilizado na maioria das aplicações Java, ele ainda é muito útil em alguns casos especiais. Ele é insubstituível quando você deseja adicionar alguns comportamentos adicionais a um objeto de uma classe existente sem alterar o código do cliente.

Alguns exemplos de proxies em bibliotecas Java padrão são:

-   `java.lang.reflect.Proxy`
-   `java.rmi.*`
-   `javax.ejb.EJB` (consulte [comentários](http://stackoverflow.com/questions/25514361/when-using-ejb-does-each-managed-bean-get-its-own-ejb-instance))
-   `javax.inject.Inject` (consulte [comentários](http://stackoverflow.com/questions/29651008/field-getobj-returns-all-nulls-on-injected-cdi-managed-beans-while-manually-i/29672591#29672591))
-   `javax.persistence.PersistenceContext`

## Estrutura do exemplo:

- some_cool_media_library/
    - ThirdPartyYouTubeLib.java
    - ThirdPartyYouTubeClass.java
    - Video.java
- proxy/
    - YouTubeCacheProxy.java

A pasta `some_cool_media_library` contém as interfaces e classes que representam uma biblioteca de terceiros de integração com o YouTube. O `ThirdPartyYouTubeLib` é a interface que define os métodos para acessar os vídeos populares e vídeos individuais. O `ThirdPartyYouTubeClass` é uma implementação concreta dessa interface.

A pasta `proxy` contém a classe `YouTubeCacheProxy`, que atua como um proxy para a biblioteca de terceiros. O proxy implementa a mesma interface `ThirdPartyYouTubeLib` e adiciona funcionalidades extras, como armazenamento em cache.

O exemplo ilustra o uso do padrão Proxy para implementar um proxy de cache para a biblioteca de terceiros de integração com o YouTube.

## Referência e Créditos

Este README foi criado com base no conteúdo do site [Refactoring Guru](https://refactoring.guru/), que fornece explicações detalhadas e exemplos de padrões de projeto, incluindo o padrão Proxy. Recomenda-se visitar o site para obter informações mais abrangentes sobre o assunto. O crédito pelo conteúdo e exemplos apresentados aqui vai para o Refactoring Guru e sua equipe.