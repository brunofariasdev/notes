[[Blazor]]

==E RECOMENDADO USAR O TEMPLATE AUTO NA CRIAÇÃO DO PROJETO E VOCÊ PODE DSCIDIR COMO USAR AO DECORRER DO DESENVOLVIMENTO.==

Caso não seja definido um Render Mode a página ira ser do SSR sem não contendo nenhuma reatividade na página.

Teremos 3 modos de renderização. 
- SERVER :  A renderização e feita do lado do servidor.
- WASM :  A renderização e feita no navegador.
- AUTO: A inteligência vai decidir como renderizar.

Os modos de renderização podem ser adicionados em 3 níveis.
 - GLOBAL :  A renderização e definida para todo o projeto.
 - PÁGINA :  A renderização e definida para toda a página.
 - COMPONENT: A renderização e definida para cada componente.


**RENDER AUTO** : O Principal problema do WASM e porque e necessário baixar os arquivos para execução do [[DOT NET]], mas com a implementação dos modos de renderização o modo RENDER AUTO traz uma solução a primeira vez que um componente ou página forem carregador ele será carregado usando o modo Server sendo assim mais rápido o carregamento liberando para o uso a aplicação.
Em segundo plano e iniciado o download do [[DOT NET]] assim que esse download for finalizado será utilizando o WASM sendo assim o melhor dos dois mundo, lembrando que o WASM espoem todos os dados da aplicação lembre-se de não deixar dados sensíveis como connection string no projeto/pagina ou componente WASM.

