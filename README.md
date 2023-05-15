# cancer-linear-regression-model-
Esse trabalho se trata da construção de um modelo de regressão linear para estimar taxas de mortalidade por câncer. O objetivo é obter a melhor acurácia e passar o modelo pelos 4 pressupostos da regressão linear.

Os dados utilizados são referentes a população dos Estados Unidos. São agregações de dados obtidos em census.gov, clinicaltrials.gov e cancer.gov. Estão disponíveis em:

A regressão linear é um método básico, mas fundamental. É amplamente utilizada em áreas diferentes. É uma técnica útil para entender relações, fazer previsões e inferências.

Aprovar uma Reg. Linear nos 4 pressupostos, significa que o modelo é estatisticamente válido. Os 4 pressupostos são:
1. O erro é uma variável aleatória com média zero;
2. A variância do erro é idêntica para todos os valores das variáveis independentes;
3. Os valores de erro são independentes;
4. O erro é uma variável aleatória com distribuição Normal refletindo o desvio entre y e o valor ajustado de y (conhecido como ŷ)

A análise de pressuposto é feita com a ajuda gráficos e testes estatísticos.

Nenhum dos modelos construídos passaram na análise de resíduos. Isso aconteceu porque o conjunto de dados possui observações com valores discrepantes nas variáveis preditoras e na variável alvo.

**Não exclui nenhum valor discrepante**, porque não encontrei um valor que parecesse ser um erro de coleta de dados. Assumi que os valores discrepantes fazem parte do comportamento dos dados. Então, seria um erro remover tais observações.

Utilizei técnicas de padronização, normalização e criação de novas variáveis com b-spline. O objetivo era superar os problemas com valores discrepantes. As tentativas não foram suficientes para aprovar o modelo nos 4 pressupostos. No entanto, as transformações foram úteis para reduzir o RMSE.

Como é sabido, a colinearidade pode ser um problema para regressão linear. Por isso, removi todas as variáveis que possuíam VIF maior que 10. Essa decisão está alinhada com o livro "Manual de Análise de Dados" de Fávero e Belfiore. 

Para estimar o erro na base de teste usei a técnica **Validação Cruzada k-Fold** para um K=10

Como o objetivo do projeto é de previsão, foi escolhido como métrica de qualidade de ajuste o RMSE. O RMSE mede o quanto o meu modelo erra, desse modo, quanto menor o RMSE mais o modelo acerta. Ao final do projeto foram avaliadas outras métricas de qualidade de ajuste.

Entregáveis do projeto:

1.   Equação do modelo final
2.   Raiz do Erro Quadrado Médio (RMSE)
3.   Diagnóstico do modelo, incluindo estatísticas e visualizações:
  *   Avaliar a linearidade do modelo (parâmetros)
  *   Avaliar a independência dos erros
  *   Avaliar a heteroscedasticidade
  *   Avaliar a normalidade da distribuição residual
  *   Avaliar a multicolinearidade

4.  Minha interpretação do modelo
