# AUTENICAÇÃO, TESTES E SEGURANÇA EM NODE.JS

### Teremos como foco explicar e entender os seguintes pontos:

  - Conceitos e fundamentos de testes;
  - O que é a cultura de testes;
  - Testes estáticos e unitários;
  - Asserções;
  - Framework de testes Jest;
  - Introduzir testes de integração com o SuperTest;


#### Testes

    Não é possível garantir que um software funcione sem a presença de erros. Existem diversos fatores que contribuem para isso como a COMPLEXIDADE, que cresce com o tamanho do projeto e o número de pessoas trabalhando. ALGORITMOS implementados de forma errada ou REQUISITOS impossíveis de serem implementados devido a limitações de harware ou software.

    Segundo Pressman, Teste é um conjunto de atividades que podem ser planejadas com atencência e executadas sistematicamente.
    Os testes tem objetivo mitigar falhas e erros que possam ocorrer em um sistema em produção a fim de garantir QUALIDADE(ISO 9126)<explicar isso dps> do software.
    Desta forma, podemos dizer que a implementação de testes na produção de softwares é um esforço coletivo que gera maior produtividade e um aumento da confiabilidade no produto.
    Ainda assim é necessário ressaltar que testes não tornam o sistema a prova de falhas.

##### Estratégias de testes de software

    As estratégias de teste de software devem ser flexíveis o bastante para promover uma estratégia de teste personalizasa e ao mesmo tepo, deve ser rígida o bastante para estimilar um planejamento razoável e companhamento à medida que o projeto progride.

    Existem diferentes estratégias(abordagens e filosofias) de testes de software, sendo que todas elas possuem as seguintes caracteristicas genéricas:

        - Para executar um teste eficaz, faça revisões técnica eficazes. Seguindo esse passo muitos dos possíveis erros serão elimninados antes do começo dos testes;

        - O teste começa no nível de componente e progride em direção à integração do sistema computacional como um todo;

        - Diferentes técnicas de teste são apropriadas para diferentes abordagens de engenharia de software e em diferentes pontos do tempo;

        - O teste é realizado pelo desenvolvedor de softwre e por um grupo de testes independentes (quando possível);

        - O teste e a depuração são atividades diferentes, mas a depuração deve ser associada a alguma estratégia de teste;


    Exemplos diferentes tipos de estratégias de software:

        - Software convencional;

        - Software orientado a objetos;

        - WebApps;

        - Aplicativos móveis;


    
##### Pirâmide de testes

    Para auxiliar na estruturação de como testar softwares é usado a chamada PIRÂMIDE DE TESTES. Sendo esta composta de três partes:

        - TESTES UNITÁRIOS, na base da pirâmide, que na maior parte são os menores componentes da base de código, que serão testados individualmente, e por isso o nome "testes unitários".

        - TESTE DE INTEGRAÇÃO, no meio da pirâmide, onde serão testadas as integrações entre as partes do projeto e algumas dependências externas.

        - TESTES END-to-END, ou E2E, são teste de ponta a ponta que se verificato tudo que está acontecendo na aplicação.

###### Testes Unitários

    O TESTE UNITÁRIO tem como objetivo testar pequenas frações de código, de um módulo, geralemnte sendo uma função ou módulo isolado. Por análisar apenas uma parte limitada do software é possivel implementar testes unitários desde o início. Apesar dessa facilidade inicial não podemos assumir que caso as diferentes funções e métodos estejam funcionando corretamente segundo os testes, o projeto/software inteiro esteja funcionando. 
    Para isso usaremos o TESTE DE INTEGRAÇÃO ou TESTE DE SERVIÇO.


###### Testes de Integração

    Pressman explica mesmo com testes unitários funcionando corretamente é possível perder alguns dados atrvés de uma interface, por exemplo quando uma função chama a outra podem faltar argumentos ou parâmetros. Ou então ao fazer uma chamda externa, um banco de dados ou algums API é possivel fazer alguns testes que vão simular e permitir ver se o comportamento dessa resposta esta de acordo com o que se espera.
    Como o nome indica esse tipo de teste tem como finalidade testar a integração entre os módulos, ou seja, se os diferentes módulos estão funcionando em conjunto.

###### Testes End-to-End

    Como explicado antes Teste End-to-End tem como objeitvo analisar o fluxo completo do projeto/software, passando por todos os módulos necessários para uma determinada ação. Por exemplo, ao fazer uma requisição de uma lista no frontend será analisado se a resposta que retornar está de acordo com o esperado.

    