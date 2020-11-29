### Projeto da Matéria de Aprendizado não Supervisionado do curso de Pós Graduação em Data Science da FURB

O objetivo do trabalho é utilizar imagens de faces disponibilizadas no dataset ORL2 junto a imagens de faces de uma nova pessoa e aplicar a técnica PCA para realizar a redução de dimensionalidade e treinar um classificador para indentificar corretamente a pessoa.

Para o desenvolvimento do trabalho foi utilizada a linguagem Python e as bibliotecas numpy, pandas, sklearn e opencv.

Para o trabalho, além das imagens da base de dados ORL disponibilizadas em aula, foram adicionadas 10 imagens da atriz Maggie Smith. Para fazer o pré processamento as imagens foram transformadas em tons de cinza, a detecção facial da atriz foi feita através do classificador haarcascade do OpenCV e por fim, as imagens das faces foram redimensionadas para o tamanho 70x80.

As imagens originais estão disponíveis na pasta "Maggie Smith - Originais", enquanto que as imagens pré processadas são disponibilizadas na pasta ORL2, junto as demais.

Foi utilizado a técnica de regressão logística para criar um classificador para identificar as pessoas com base no resultado do PCA. O dataset foi dividido utilizando holdout com 70% dos dados para treino e 30% para teste, estratificando a divisão pela pessoa. A métrica utilizada para a avaliação foi acurácia. O PCA foi aplicado somente sobre os dados de treino para não enviesar o experimento. O experimento foi executado variando o número de componentes principais entre 10 e 20, obtendo-se os seguintes resultados:

- 10 componentes principais, acurácia: 93.50%.
- 11 componentes principais, acurácia: 93.50%.
- 12 componentes principais, acurácia: 93.50%.
- 13 componentes principais, acurácia: 95.12%.
- 14 componentes principais, acurácia: 95.12%.
- 15 componentes principais, acurácia: 95.93%.
- 16 componentes principais, acurácia: 95.93%.
- 17 componentes principais, acurácia: 96.75%.
- 18 componentes principais, acurácia: 96.75%.
- 19 componentes principais, acurácia: 95.93%.
- 20 componentes principais, acurácia: 97.56%.

Por fim, é montado um classificador com o número de componentes que obteve a maior acurácia para avaliar os erros do modelo.

Para reproduzir os resultados, basta abrir o projeto no google colab, criar as pastas "Maggie Smith - Originais" e "ORL2" e fazer os uploads de seus respectivos conteúdos, e executar o notebook.
