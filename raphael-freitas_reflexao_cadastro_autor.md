### [Sobre ser melhor estudante](https://github.com/claudiooliveirazup/documentacao-cartao-branco/blob/master/leitura-obrigatoria-preparo-desafios/0-0-1-preparo-aprendizado.md)

Para um melhor aprendizado, filtrar as informações irrelevantes, reduzindo o espaço de busca e por consequência diminui o esforço necessário para aprender. Isso evita de desperdiçar energia com esforços desnecessários. Outras estratégias para estudo um assunto são:
*	Elaborar perguntas sobre o que você está estudando;
*	Escrever tudo o que você lembra sobre o assunto;
*	Explicar parte do assunto para alguém;
*	Resumir o que você estudou;
*	Fazer um diagrama relacionando os elementos importantes sobre aquele assunto.
  
A memória é mais do que um repositório de informações, ela é constituída por memória de trabalho e memória de longo prazo. Assim temos:
*	Memória de trabalho: É um local onde colocamos as informações que queremos processar e manipular. Ela é limitada a quantidade e ao tempo de retenção de informações.
*	Memória de longo prazo: Pode armazenar uma quantidade ilimitada de informações por um longo período, porém não conseguimos manipular seu conteúdo sem que seja transferido para a memória de trabalho. A memória grava as informações em forma de esquemas, ficando mais fácil ter acesso a essas informações.

A teoria da carga cognitiva mostra que, existem dois tipos de cargas:
*	Carga intrínseca: Se refere a complexidade de informações que preciso lidar.
*	Carga extrínseca: Se refere a carga não ligada diretamente ao que está sendo aprendido no momento

As duas cargas competem para a capacidade de memória de trabalho que temos, prejudicando o aprendizado.

Assim como também ter um objetivo definido e uma direção para ser alcançada são fundamentais. Então, para atingir chegar no objetivo é necessário muito treino antes da prática. Focar na competição todos os dias não te permite melhorar, de evoluir o aprendizado, assim, quanto mais terei treinado para criar novos códigos, resolver bugs, realizar uma manutenção evolutiva (refatoração) e entendimento do código de outros desenvolvedores, mais estarei preparado para as situações adversas que se pode encontrar no dia a dia. E uma das coisas fundamentais é nunca se comparar aos outros e sim se inspirar neles.

### [Sobre CDD](https://github.com/claudiooliveirazup/documentacao-cartao-branco/tree/master/leitura-obrigatoria-design-codigo)

O CDD (Cognitive-Driven development) pode contribuir para reduzir o esforço necessário para manutenção e correção de falhas. Uma estratégia para isso é dividi-lo em blocos mais compreensíveis. No entanto, a complexidade do software aumenta à medida que novos recursos são incorporados, impactando sua manutenibilidade. Portanto, a separação da responsabilidade do componente deve considerar não apenas o domínio, mas também a complexidade cognitiva do software. Estudos realizados indicam que os humanos conseguem manter apenas sete unidades de informação na memória de curto prazo, e esse limite pode ser aplicado no desenvolvimento de software. A sobrecarga cognitiva ocorre quando se precisa adicionar mais recursos para arrumar bug, melhorar design ou otimizar o uso de recursos. Se um ponto do código com carga intrínseca no limite usa uma entity com carga intrínseca baixa, pode ser um sinal de má distribuição.

A distribuição da carga intrínseca pode ser atribuída da seguinte forma:
*	Classes com atributos de dependência (@Controller e @Service) devem ter no máximo 7 pontos de carga intrínseca;
*	Classes com atributos de dados, devem ter no máximo 9 pontos de complexidade (Ex.: Entities);
*	Acoplamento com classes específicas contam 1 ponto (Ex.: @Autowired);
*	Infrastructure Services e classes de configuração podem ter a pontuação que quiser;
*	Repository deve ter no máximo 3 pontos.
*	Toda branch conta 1 ponto (Ex.: if, else, loops, switch, case, try, catch, etc.);
*	Toda passagem de função como argumento conta 1 ponto (Ex.: Lambdas e method reference);

Utilização do CDD em contextos atuais:
*	Para classes que já existem aceite o fato da complexidade que já está lá devemos pontuar e colocar objetivos de refatoração para diminuir a complexidade de entendimento.
*	Para classes novas podemos estabelecer o limite restritivo;
*	Para manutenção, corretiva ou evolutiva, já deve ser levado em consideração o limite restritivo e construir novos códigos pontuando-o.

### [Sobre o conjunto de técnicas de código](https://github.com/claudiooliveirazup/documentacao-cartao-branco/tree/master/informacao-suporte-design)

Para ser fazer a implementação de técnicas e design de código se deve:
*	Fazer um código que funcione e que seja entendível;
*	Dominar o negócio, a linguagem de programação, os frameworks e bibliotecas;
*	Executar o código o mais rápido possível para encontrar bugs e corrigir rapidamente;
*	Proteger a borda do sistema, ou seja, realizar a validação e tratamento das informações recebidas da entrada, pois não controlamos a informações vinda do cliente;
*	Separar a borda externa do sistema com o domain, evitando ataques como “Mass Assignment”. Além de separar classe de domínio que é utilizado no projeto inteiro com o que é usado naquele local específico;
*	Não serializar objetos de domínio para as respostas de API, pois qualquer modificação na classe de domínio irá afetar a saída, assim evitando a quebra de contrato. O ideal é criar uma classe específica de resposta;
*	Indireções aumenta a complexidade, ou seja, quanto mais classes novas eu crio no projeto mais unidades de informação precisa entender, depende do contexto;
*	Utilizar construtores para criar o objeto, assim, permite guiar o desenvolvedor e deixar o código menos democrático. Só criar construtores sem parâmetro quando realmente for necessário e se, no caso de frameworks necessitar da utilização do construtor sem argumentos, utilizar a anotação deprecated.
*	Deixar pistas como a utilização da validação do Bean Validation para criação de um model. As anotações no construtor por exemplo não serão validadas, mas servirão como dicas;
*	A complicação do código é proporcional a complicação da feature, por isso a linha de design deve visar sempre diminuir a carga cognitiva;
*	Usar tudo o que se é conhecido. Apenas criar código novo quando for necessário;
*	Não usar exception para controle de fluxo pois as exceptions foram criadas para situações não imaginadas. Cada classe de exception aumenta 1 ponto de complexidade. A solução é criar um objeto que tenha dois possíveis retornos;
*	Criar testes automatizados para encontrar e consertar bugs;

### [Sobre cada funcionalidade implementada](https://github.com/rafreitas94/bootcamp-01-template-casa-do-codigo)

TODO
