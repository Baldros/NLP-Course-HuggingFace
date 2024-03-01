# Introdução:
No Capítulo 1, vimos que os modelos Transformer geralmente são muito grandes, com milhões a dezenas de bilhões de parâmetros, tornando o treinamento e a implementação desses modelos se torna uma empreitada complicada. Além disso, com novos modelos sendo lançados quase diariamente, cada um com sua própria implementação, experimentá-los não é uma tarefa fácil.

A biblioteca 🤗 Transformers do ecossistema Hugging Face foi criada para resolver esse problema. Seu objetivo é fornecer uma API única por meio da qual qualquer modelo Transformer possa ser carregado, treinado e salvo. As principais características da biblioteca são:

**1. Facilidade de uso:** Baixar, carregar e usar um modelo de **processamento de linguagem natural (NLP)** de última geração para inferência pode ser feito em apenas duas linhas de código.

**2. Flexibilidade:** No núcleo, todos os modelos são classes simples PyTorch nn.Module ou TensorFlow tf.keras.Model e podem ser manipulados como qualquer outro modelo em seus respectivos frameworks de aprendizado de máquina (ML). Esse é um ponto muito importante que deve ser internalizado, afinal de contas, nenhum modelo vem pronto, precisamos ajusta-los a nossas necessidades.

**3. Simplicidade:** Quase nenhuma abstração é feita em toda a biblioteca. O conceito central é o "Tudo em um arquivo": a passagem direta de um modelo é inteiramente definida em um único arquivo, para que o código em si seja compreensível e modificável.

Essa última característica torna a 🤗 Transformers bastante diferente de outras bibliotecas de ML. Os modelos não são construídos em módulos compartilhados entre arquivos; em vez disso, cada modelo tem suas próprias camadas. Além de tornar os modelos mais acessíveis e compreensíveis, isso permite que você experimente facilmente em um modelo sem afetar outros. Entender esse funcionamento é muito importante para a implementação dos modelos que constam no ecossistema Hugging Face. 

## Conteudo do Capítulo:
Este capítulo começará com um exemplo de ponta a ponta em que usamos um modelo e um **tokenizador** juntos para replicar a função pipeline() apresentada no Capítulo 1. Em seguida, discutiremos a API do modelo: mergulharemos nas classes de modelo, configuração e mostraremos como carregar um modelo e como ele processa entradas numéricas para produzir previsões.

Em seguida, examinaremos a **API do tokenizador**, que é o outro componente principal da função pipeline(). Os **tokenizadores** cuidam das primeiras e últimas etapas de processamento, lidando com a **conversão de texto para entradas numéricas** para a rede neural e a conversão de volta para texto quando necessário. Finalmente, mostraremos como lidar com o envio de várias sentenças por meio de um modelo em um lote preparado e concluiremos com uma análise mais detalhada da função de alto nível tokenizer().
