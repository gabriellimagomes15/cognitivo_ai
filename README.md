# cognitivo_ai
Repository for test cognitivo ai

### a. Como foi a definição da sua estratégia de modelagem? Para elaborar o modelo para classificação, segui os seguintes passos:
  - Exploração da base de dados;
  - Corrigi alguns registros inconsistentes na coluna alcohol;
  - verifiquei a distribuição de todos os atributos;
  - verifiquei a correlação entre os atributos;
  - criei 3 subsets:
    - um com os dados originais;
    - um com os dados normalizados;
    - um com os dados normalizados e balanceados;
  - fiz transformação da variavél target (quality) para 3 classes (ruim, bom, ótimo) e outra com 2 classes (ruim, ótimo)
  - executei diferentes algoritmos de classificação;
  - ao final foi selecionado apenas um algoritmo (ExtraTreesClassifier);
  - foi feita a validação desse algoritmo com base no reporte (accuracy, matrix confusion, auc curve, precision, recall e f1 score);
  - o modelo final foi salvo em joblib.
  
### b. Como foi definida a função de custo utilizada? Foi utilizada a cross-validation para função de custo do modelo.

### c. Qual foi o critério utilizado na seleção do modelo final? 
Com base nas informações: accuracy, matrix confusion, cross-validation, precision, recall e principalmente na métrica f1 score.

### d. Qual foi o critério utilizado para validação do modelo? Por que escolheu utilizar este método? 
O modleo final escolhido é de classificação binária, então, para validação foi utilizada a AUC Curve e a métrica de f1score.
A AUC Curve demonstra de forma fácil e confiável como está a curva de aprendizado do modelo, o qual indica que este modelo não sofreu underfitting e nem overfitting, e a métrica F1 Score possibilitar confirmar a qualidade do modelo porque faz uma média da 'precision' e 'recall', tendo um resultado consideravelmente bom. 

### e. Quais evidências você possui de que seu modelo é suficientemente bom? 
Com base na confusion matrix, auc curve e f1 score, estão com bons resultados, o que indica que o modelo não sofreu underfitting e nem overfitting, 
