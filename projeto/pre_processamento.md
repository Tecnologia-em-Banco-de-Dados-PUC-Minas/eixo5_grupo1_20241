# 3ª Etapa - Pré-Processamento de Dados

## Entendendo a Base de Dados
A base de dados cedida pelo Spotify possui informações categorizadas como 'features'. Seu significado está disponível na página [Spotify for Developers](https://developer.spotify.com/documentation/web-api/reference/get-audio-features). As principais abordads neste trabalho são:

* **Tom (_Key_)**: o tom principal em que a música é tocada. Seu formato está em notação _American Standard Pitch Notation (ASPN)_, ou seja, em notação padrão americana de altura. Consiste basicamente especificar a altura do som, associando uma nota musical ou sua letra representativa a um número que identifica a oitava da nota.Se a nota não for detectada, o valor é -1. Valores são apresentados como números inteiros (_integer_).
<div align="center">
<img src="/imagens/Integer-Circle.001.png" width="400" height="200">
</div>

* **Acusticidade (_acousticness_)**: medida de confiança de 0,0 a 1,0 para saber se a faixa é acústica. 1,0 representa alta confiança de que a faixa é acústica. Valores são decimais (_float_).
* **Dançabilidade (_danceability_)**: descreve o quão adequada uma faixa é para dançar com base em uma combinação de elementos musicais, incluindo andamento, estabilidade do ritmo, força da batida e regularidade geral. Um valor de 0,0 é menos dançante e 1,0 é mais dançante. Valores são decimais (_float_).
* **Energia (_energy_)**: medida de 0,0 a 1,0 e representa uma medida perceptiva de intensidade e atividade. Normalmente, as faixas energéticas parecem rápidas, altas e barulhentas. Por exemplo, o death metal tem alta energia, enquanto um prelúdio de Bach tem pontuação baixa na escala.Valores são decimais (_float_).
* **Instrumentalidade (_instrumentalness_)**: prevê se uma faixa não contém vocais. Os sons “Ooh” e “aah” são tratados como instrumentais neste contexto. Faixas de rap ou palavras faladas são claramente “vocais”. Quanto mais próximo o valor da instrumentalidade estiver de 1,0, maior será a probabilidade de a faixa não conter conteúdo vocal. Valores acima de 0,5 pretendem representar faixas instrumentais, mas a confiança é maior à medida que o valor se aproxima de 1,0.Valores são decimais (_float_).
* **Vivacidade (_liveness_)**: Detecta a presença de um público na gravação. Valores mais altos de vivacidade representam uma probabilidade maior de que a faixa tenha sido tocada ao vivo. Um valor acima de 0,8 oferece forte probabilidade de que a pista esteja ativa.Valores são decimais (_float_).
* **Altura Volume (_loudness_)**: O volume geral de uma faixa em decibéis (dB). Os valores de intensidade são calculados em média em toda a faixa e são úteis para comparar a intensidade relativa das faixas. Loudness é a qualidade de um som que é o principal correlato psicológico da força física (amplitude). Os valores típicos variam entre -60 e 0 db. Valores são decimais (_float_).
