# HIML
Hands on Introduction to Machine Learning
<br />
HIML_Final_MonteCarlo.ipynb <br />
featuresTSFRESH_fault.txt <br />
featuresTSFRESH_nom.txt <br />
df_columns.csv <br />

Notebook HIML_Final_MonteCarlo.ipynb para extração de características usando TSFRESH, treinamento e avaliação de modelos de aprendizado de máquina <br />
usando busca aleatória de hiperparâmetros e Monte Carlo. <br />
 <br />
O notebook é divido em 5 seções, descritas em detalhes abaixo. <br />
 <br />
Nota: a extração de características com o tsfresh dura aprox. 4 horas para cada classe.  <br />
Os dados resultantes da extração foram salvos no arquivo featuresTSFRESH_fault.txt e featuresTSFRESH_nom.txt <br />
para facilitar a reprodução dos resultados.  <br />
Na seção 3, os arquivos .txt são lidos, sem a necessidade de rodar as seções 1 e 2. <br />
 <br />
1. Leitura e tratamento de dados de entrada referentes a casos de falha: <br />
 <br />
Leitura de arquivos .csv da classe 4 do dataset 3W, e extração de características usando <br />
rolling window e tsfresh. (~4h de duração) <br />
 <br />
2. Leitura e tratamento de dados de entrada referentes a casos nominais: <br />
 <br />
Leitura de arquivos .csv da classe 0 do dataset 3W, e extração de características usando <br />
rolling window e tsfresh.(~4h de duração) <br />
 <br />
3. Leitura das features em arquivos texto: <br />
 <br />
Os arquivos txt salvos são lidos e salvos na estrutura featuresTSFRESH, usada como dado de entrada para o treinamento dos  <br />
modelos. <br />
Algumas das características (médias, medianas e RMS das séries de pressão) são selecionadas para visualização com violin plots. <br />
 <br />
4. Modelo de aprendizado de máquina: <br />
 <br />
Treinamento preliminar dos modelos de aprendizado na seguinte ordem <br />
Linear Regression, SVC com Kernel linear, SVC com busca de hiperparâmetros (~30min de duração), SVC com kernel polinomial, <br />
SVC com kernel gaussiano, Random Forest, e Random Forest com busca de hiperparâmetros (~15min de duração). <br />
 <br />
5. Monte Carlo <br />
 <br />
Uso do método de monte carlo para avaliação dos modelos usando as métricas Accuracy, F1 score, Recall e Average score. <br />
Os resultados são apresentados usando violin plots. <br />
