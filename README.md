# APP-Ada-Pela-Paz
Aplicacao de exploracao de dados e predicao de nivel de risco

#################################################
Primeira versao do preditor de risco
################################################

./V0_Working/ 

---Exploracao e geracao de dados
   Calculo do risco baseado em probabilidades de ocorrencia por estado e idade 

Data_Exploration.R e Data_Merge.ipynb

Input Data: ./Dados/MeusDados/BASE 13 - Feminicidio Por UF e Cor/
 
            Homicidios por Idade e genero em 2014.xlsx
            Taxa Homicídios de mulheres brancas(por 1000 habitantes) por UF_2003a2013.xlsx
            Taxa Homicídios de mulheres negras(por 1000 habitantes) por UF_2003a2013.xlsx  
            Resumo --> HEG.csv, ELL.csv, TB.csv, TN.csv

Outputs: ./Dados/MeusDados/  
       
        df_lugar_raca_risco.csv (input para Data_Merge.ipynb)
        df_estado_raca_idade.csv (output of Data_Merge.ipynb)
        df_estado_raca_idade_fin.csv (input data para o treinamento da rede neural)

---Modelo de Rede Neural: 

PreditorDeRisco.ipynb
 
features: Estado, Cor da pele, Edade
label: Nivel de Risco

Input: ../Dados/MeusDados
       
       df_estado_raca_idade_fin.csv (input data para o treinamento da rede neural)
       APP - Ada Pela Paz (Pesquisa).csv (Google Form, input data para predicao do nivel de risco)

Outpus: ./V0_Working/
        
        DataUsuarios.csv (informe de resultados)
        RetroData.csv (dados iniciais mais novos resultados, retroalimentacao da red neural) 


#################################################
Segunda versao do programa para testes de optimizacao
#################################################

./V1_test/ 

procurado optimizar a rede neuronal desconsiderando casos pouco

atencao nos peaks das diferencas porcentuais (poucos pontos para valores extremos de risco)

#################################################
Terceira versao do programa para testes de optimizacao
#################################################

./V2_test/

Mais dados !! para melhorar a predicao da rede neural

