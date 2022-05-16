# Aplicação do Desafio
**By Fabio Marsiaj**

Em cada um dos serviços o objetivo é diferente:
 - No serviço A, o acesso ao banco de dados deve ser feito de forma segura por causa dos dados sensíveis. 
   Por essa razão decidi criptografar a senha do único usuário ADMIN para segurança no banco (no caso eu não precisava
   mexer em config de banco pro desafio). E foram feitas configurações de autenticação e autorização para a request.
 - O serviço B não exige um acesso tão seguro e tão rápido.
 - O serviço C, não exige segurança e deve ser feito de forma mais rápida possível. Por essa razão decidi usar o Spring Webflux
   para chamadas assíncronas bem como o spring Reddis, para cachear as chamadas do banco, fazendo com que na próxima chamada a consulta
   seja mais performática.

## Summary

- [Tecnologias](#tecnologias)
- [Requisitos](#requisitos)
- [Considerações](#consideracoes)
- [Autor](#autor)

## Tecnologias

Para este projeto criei as aplicações com Spring Boot Web, Spring WebFlux, Spring Reddis e MongoDB para persistência.


## Requisitos

- [Git](https://git-scm.com/)
- [MongoDB](https://www.mongodb.com/download-center)
- [JDK11](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html)

## Considerações

Com mais tempo poderia ter utilizado outras tecnologias, como conteinerizar os serviços com docker e utilizar a própria AWS para armazenar as informações.
Ou até mesmo o https://strapi.io/ para disponibilizar as informações do banco.

Não sei se o objetivo era ter interações entre os serviços, por exemplo, o serviço C precisava de informações de movimentação do cpf - que estava
no serviço A e também de informações das rendas que estava no serviço B.


## Autor

**Fabio Quinto Marsiaj** -  [GitHub](https://github.com/fabioqmarsiaj)

   <a href="https://github.com/fabioqmarsiaj">
        <img 
        alt="Imagem do Autor Fabio Marsiaj" src="https://avatars0.githubusercontent.com/u/34289167?s=460&v=4" width="100">
  </a>
  