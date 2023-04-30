# Curso Full Cycle 3.0 - Módulo Comunicação entre sistemas

<div>
    <img alt="Criado por Alcir Junior [Caju]" src="https://img.shields.io/badge/criado%20por-Alcir Junior [Caju]-%23f08700">
    <img alt="License" src="https://img.shields.io/badge/license-MIT-%23f08700">
</div>

---

## Descrição

O Curso Full Cycle é uma formação completa para fazer com que pessoas desenvolvedoras sejam capazes de trabalhar em projetos expressivos sendo capazes de desenvolver aplicações de grande porte utilizando de boas práticas de desenvolvimento.

---

## Repositório Pai
https://github.com/alcir-junior-caju/study-full-cycle-3-0

---

## Visualizar o projeto na IDE:

Para quem quiser visualizar o projeto na IDE clique no teclado a tecla `ponto`, esse recurso do GitHub é bem bacana

---

#### Comunicação entre sistemas

Um dos pontos mais críticos de se trabalhar com Microservices, é a comunicação entre sistemas, geralmente sempre é usado umas ou duas formas de comunicação para estabelecer comunicações entre sistemas. Isso na maioria das vezes podem trazer grandes problemas, então sempre é interessante saber que existem outras maneiras de comunicação entre sistemas e saber quando utilizar.

Em Microservices muitas das vezes o mais interessante é ter comunicações assincronas, deixando assim os serviços mais idependentes e mais resilientes.

Geralmente cada microservice tem seu próprio banco de dados deixando o serviço mais idependente, quando se trabalha com comunicação assincrona podemos ter dois serviços que tenham dados inconsistentes, por exemplo o serviço de produtos com várias informações e o serviço de checkout que apenas persistiu o nome e id do produto, caso o produto sofra uma alteração, essa alteração se vai se refletir em tempo real em checkout, com isso temos uma incossistência eventual.

#### REST
- Muitos desenvolvedores "já sabem trabalhar com REST";
- REST (Representational State Transfer);
- Surgiu em 2000 por Roy Fielding em uma dissertação de doutorado;
- Simplicidade;
- Stateless;
- Cacheável;

#### REST: Níveis de maturidade (Richardson Maturity Model)
- Nível 0: The Swamp of POX;
- Nível 1: Resources;
- Nível 2: HTTP Verbs;
- Nível 3: HATEOAS (Hypermedia as the Engine of Application State);

***[Artigo](https://www.brunobrito.net.br/richardson-maturity-model/)***

#### REST: Uma boa API REST
- Utiliza URIs únicas para serviços e itens expostos para esses serviços;
- Utiliza todos os verbos HTTP para realizar as operações em seus recursos, incluindo caching;
- Provê links relacionais para os recursos exemplificando o que pode serfeito;

#### REST: HAL, Collection + JSON e Siren
- JSON não provê um padrão de hipermídia para realizar a linkagem;
- HAL: Hypermidia Application Language;
- Siren;

#### REST: HTTP Method Negotiation
- HTTP possuí um outro método: OPTIONS;
- Esse método nos permite informar quais métodos são permitidos ou não em determinado recurso;

#### REST: HTTP Content Negotiation
- O processo de Content Negotiation é baseado na requisição que o client está fazendo para o server. Nesse caso ele solicita o que e como ele quer a resposta. O server retornará ou não a informação no formato desejado;
- Client solicita a informação e o tipo de retorno pelo server baseado no media type informado por ordem de prioridade;
- Através de um content-type no header da request, o servidor consegue verificar se ele irá conseguir processar a informação para retornar a informação desejada;
