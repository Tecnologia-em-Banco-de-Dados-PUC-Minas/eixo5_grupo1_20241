## 4ª Etapa
###  Aprendizado de máquina

Para a realização deste trabalho, optou-se por estruturar as bases de dados em um modelo Star Schema, devido ao entendimento de que essa estrutura de dados permitiria um melhor aproveitamento e otimização dos dados. 

## Preparação do Google Colab

Com as bases de dados organizadas dentro do Google Drive, foi preciso preparar o ambiente de dados do Colab do Google para a vinculação com as bases.

Para isso, foi preciso importar as seguintes bibliotecas do Python: pandas, numpy e google.colab.

Na sequência, foi preciso importar a conexão do Colab com o Drive do Google.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/a523d31e-1f48-4e2e-8154-02f0e2e5d482)

### Importando as bases e criando os DFs

Com o ambiente preparado para a execução dos códigos, foram importadas as bases de dados que acabaram transformadas em Data Frames.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/793df2fe-0b11-4394-9c8d-7a4e82cd928c)

Após a criação dos Data Frames, houve a checagem para garantir a importação.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/f66d6aa2-cd6d-4b20-881d-eeaf31923dd1)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/55df66ae-af36-41d2-849e-ceef960ea26f)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/45b08841-4dc9-444e-918e-ddfa89449a1b)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/00f4a65d-bf06-4b67-a486-9a83ac47185d)

Garantida a importação correta dos dados e a execução adequada dos DF, checou-se os metadados - as informações das bases.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/4f3864b0-2960-40e7-9aad-826bf7bb336a)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/68c4ff95-3832-46c9-89ba-60e6465f20a3)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/6ed8cc68-79c7-4fb9-b86c-ebf3cfd2f864)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/af7312a6-9ac4-400d-87bb-27dccdd26e0a)

### Pré-processamento dos dados

A fase do pré-processamento visou garantir a correta transformação dos dados para assegurar que os modelos de aprendizado de máquina rodassem em uma base uniforme, sem valores nulos, além de realizar os merges entre as bases.

A primeira etapa padronizou os títulos dos DFs.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/7e563464-8373-473a-bdf2-3bc57d2f767f)

Depois, verificou-se as colunas que eram comuns entre os DFs para estabelecer, posteriormente, quais seriam utilizadas nos treinamentos e análises e quais seriam excluídas.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/ab69e087-7d9e-4aeb-b09c-a7505099c48e)

As duas etapas seguintes visaram garantir a qualidade dos dados que seriam processados, removendo valores duplicados e nulos.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/7bb48471-5a28-4ec8-a0ba-1cef8b371008)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/84f8aac6-fe5b-44f2-befd-a2566908351c)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/b2819376-34fb-4c22-8f03-11ce56cbada6)

### Testes de predição

Nesta etapa, o grupo utilizou uma base de dados que continha as músicas mais populares no Spotify e a base de dados com as músicas mais tocadas de 2023. Isso foi feito para testar um calculo de popularidade, que não existia em uma das bases. Para isso, uniu-se as duas bases e foi aplicada técnicas de ML nas músicas que eram comuns às duas bases e, assim, buscar realizar um cálculo de popularidade nos valores que eram nulos.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/579ee17c-1ed0-44c7-aa0b-49f4d271c8d6)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/8bb2cb09-38d1-433c-9e3c-0dbb4feb01bf)

No entanto, a tentativa de criar essa métrica de popularidade para as músicas de 2023, para deixá-las com esse valor referenciado, não deu certo. O dado não pareceu ter qualidade suficiente para ser equiparável à métrica calculada pelo Spotify, que estava presente na base de dados de 2000 até 2022.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/5fc4d607-312f-4ac4-8f19-99996e6caaca)

O cálculo em questão utilizava o "Steams" como métrica de referência.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/98aabfcb-14a5-4fb0-9fa6-582585c1d022)

### Explorando correlações e configurando os modelos de aprendizado de máquina

Com a tentativa de criar uma métrica de popularidade não obtendo sucesso, o próximo passo foi configurar os DFs para buscar correlações e configurar os ambientes de aprendizado de máquina.

Usando a base de dados do Spotify, buscou-se observar possíveis correlações entre a popularidade de uma música e demais características.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/ced3e3e4-81d6-454a-9f51-6b83865ba53a)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/5052c8ee-7e1f-46c7-9b8a-402eaa37eacc)

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/2008a801-99b6-4e8d-94c6-0edb72e052fc)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/5f62427e-31af-4c30-9361-46a6167d2fc3)

Identificadas as correlações mais fortes entre popularidade e demais atributos musicais, passou-se para a preparação das bases de dados para que elas fossem configuradas em diferentes modelos de ML.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/dce53c8d-5b9d-4fe9-bc28-7f3f5c0c4ca1)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/f1658465-4a74-4892-9ef1-eee9ed0fdd78)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/f5331e6b-5ed0-4dc4-8fd0-69c2881b3ff7)

Para poder utilizar os modelos de ML, os DF precisaram passar pelo processo de one-hot-encondig para preparar as features categóricas para o ML.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/624f450a-8707-45c7-945a-51dd560830fc)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/b60cfca8-e17d-420a-9693-ef757f51303c)
![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/67fc3752-eb52-465b-b4eb-c530bdd5d088)

Depois, normalizou-se os dados numéricos.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/0a72b954-b640-41c0-820d-ca925b6e111a)

E dividiu-se os conjuntos de aprendizado e de teste.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/5a902f39-f6f4-4a29-941c-9b19acc532ce)

Com o ambiente e os DF preparados, o primeiro modelo de ML testado foi o KNN.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/a7a1d9ab-d7ac-4e02-9b6d-cd72915f3f91)

O erro médio quadrático foi alto, porém, mais tarde, observou-se que, dos testes, ele foi o menor.

O segundo modelo foi o DecisionTree.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/4d3f74f1-00e1-4cce-b42f-90a5161d418f)

Por fim, testou o modelo de LinearRegression.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/89575bb0-5969-45d5-b1de-da6739e945d5)

Com os modelos de aprendizado de máquina configurados e os erros médios quadráticos explanados. O próximo passo foi ver a importância de cada feature musical segundo os modelos de DecisionTree e LinearRegression.

![image](https://github.com/Tecnologia-em-Banco-de-Dados-PUC-Minas/eixo5_grupo1_20241/assets/138826075/5772dc96-c2f1-4d32-b1fc-dcb9cd30ab8d)

