# Ifood_Churn
Estudo de Churn de clientes na plataforma do Ifood. 

## Definição do Problema

<div align="justify">
  <p>O departamento de CRM/Marketing do iFood fez uma solicitação para o time de Ciência de Dados (que estão atrelados ao time de dados dentro da área de TI) para criar um modelo de Machine Learning para prever os clientes que darão Churn.
  </p>
  <p>O objetivo deles com o modelo é atuar sobre os clientes com maiores chances de darem churn no próximo mês.</p>
  <ul>
    <li>A ação será realizada 1 vez por mês, todo dia 01.</li>
    <li>Como a frequência de compras dos clientes do IFood é relativamente alta, então ficou-se decidido na reunião com a área cliente que o modelo seria construído usando features construídas em um período fechadode 1 mês para prever se um dado cliente irá deixar de comprar (churn) no próximo mês.</li>
  </ul>
  <p>A métrica principal de avaliação do modelo é a AUC, dado que o score gerado pelo modelo será usado para ordenar a base.</p>
</div>

## Conclusão
<div align="justify">

  <p>Variável mais importante e como ela se relaciona com a "target"</p>
  
  <ul>
      <li>A variável "qtd_pedidos_1m" é a mais importante, embora as outras estejam ali bem próximas em termos de importância.</li>
      <li>Quantos mais pedidos foram realizados no mês anterior, maior é a chance de se não comprar no mês seguinte. Bastante interessante, né? Isso provavelmente acontece porque se um cliente gasta muito no mês anterior, ele tende a não gastar no mês seguinte devido a orçamento financeiro. Será que faz sentido aumentar o tempo de criação tanto do target quanto das features?</li>
  </ul>
  
  <p>Como as outras variáveis se relacionam com a variável target?</p>
  
  <ul>
    <li>"recencia": quanto menor a recência, maior é a chance de comprar no próximo mês (outro indicativo de que talvez precisemos aumentar os meses da safra para criação das features e do target).</li>
    <li>"receita_1m": quanto maior a receita (gasto do cliente), maior é a chance de comprar no próximo mês.</li>
  </ul>
</div>

<div align="center">
  <p>Shap Summary</p>
  <img src="https://github.com/Lucas-Sobreira/Ifood_Churn/blob/main/arquivos/shap_sumary.png"/>
</div>
