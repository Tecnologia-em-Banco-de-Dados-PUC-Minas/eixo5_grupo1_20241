## 4ª Etapa
###  Aprendizado de máquina

Para a realização deste trabalho, optou-se por estruturar as bases de dados em um modelo Star Schema, devido ao entendimento de que essa estrutura de dados permitiria um melhor aproveitamento e otimização dos dados. 

## Preparação do Google Colab

Com as bases de dados organizadas dentro do Google Drive, foi preciso preparar o ambiente de dados do Colab do Google para a vinculação com as bases.

Para isso, foi preciso importar as seguintes bibliotecad do Python: pandas, numpy e google.colab.

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




