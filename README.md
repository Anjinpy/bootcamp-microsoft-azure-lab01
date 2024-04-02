# Prevendo Aluguéis de Bicicletas com Microsoft Azure

## Introdução

Este guia aborda a criação de um modelo de previsão para aluguéis de bicicletas utilizando o Microsoft Azure Machine Learning. Antes de iniciar, certifique-se de ter uma conta no Microsoft Azure. Caso não possua, siga [este link](https://azure.microsoft.com/pt-br/free/) para criar uma.

## Configurando o Espaço de Trabalho

1. Acesse o [Portal do Azure](https://portal.azure.com) e faça login com suas credenciais da Microsoft.
2. Crie um novo recurso do Azure Machine Learning, preenchendo os campos necessários, como nome, região, grupo de recursos, entre outros.
3. Após a criação, acesse o recurso implantado e selecione "Launch Studio" ou navegue até [https://ml.azure.com](https://ml.azure.com) para acessar o Azure Machine Learning Studio.

## Treinando o Modelo com Aprendizado de Máquina Automatizado

1. No Azure Machine Learning Studio, acesse a página "ML Automatizado".
2. Crie um novo trabalho de ML automatizado, configurando as seguintes opções:
  - **Básico**: Nome do trabalho, experimento e descrição.
  - **Tipo de Tarefa e Dados**: Selecione "Regressão" como tipo de tarefa e carregue o conjunto de dados de aluguéis de bicicletas fornecido.
  - **Configurações de Tarefa**: Defina os parâmetros de treinamento, como métrica primária, modelos permitidos e limites de tempo e recursos.
  - **Computação**: Escolha o tipo de computação, como sem servidor ou máquina virtual.
3. Envie o trabalho de treinamento e aguarde sua conclusão.

## Avaliando e Implantando o Modelo

1. Após a conclusão do treinamento, revise o "Melhor Resumo do Modelo" e visualize as métricas e gráficos de desempenho.
2. Implante o melhor modelo como um serviço web, definindo um nome, descrição e tipo de computação.
3. Aguarde a implantação ser concluída com sucesso.

## Testando o Modelo Implantado

1. No Azure Machine Learning Studio, acesse a seção "Endpoints" e abra o endpoint em tempo real do modelo implantado.
2. Na guia "Teste", substitua os dados de entrada de exemplo pelo JSON fornecido com as características desejadas para previsão.
3. Clique em "Testar" e revise os resultados, que incluirão o número previsto de aluguéis de bicicletas com base nos dados de entrada.

## Conclusão

Parabéns! Você criou, treinou e implantou com sucesso um modelo de previsão para aluguéis de bicicletas utilizando o Microsoft Azure Machine Learning. Lembre-se de excluir os recursos criados após os testes, caso tenha utilizado uma conta gratuita, para evitar cobranças adicionais.
