# GNNs na neurociência: redes convolucionais de grafos para análise de ressonância magnética funcional
Este repositório é uma aplicação do projeto e modelo do paper de Sidney Hough, Julian Quevedo, e Pino Cholsaipant como parte do projeto de curso Stanford CS224W.

Adaptado por Nathan Gonçalves e Ulysses Monte para o Trabalho final da disciplina de Redes Complexas e GNN;
Professor Sérgio Nery;
IFES 2025.1 BSI.

# Como executar
Este repositório pode ser executado normalmente em ordem no próprio Google Collab
Provavelmente para executar a Seção Bônus você deve assinar o Collab Pro, mas fica a seu critério baixar e rodar na sua própria máquina

# Objetivo Geral
*Do projeto* : Desenvolver conceitos aprendidos na disciplina em um projeto real com o auxílio de um Paper já completo e publicado, com dataset disponível.
*Do Sistema* : Treinar uma Rede neural para reconhecer padrôes observados no funcionamento do cérebro humano via Ressonância magnética funcional e aprender a diferenciar se cperebro é de um adulto ou de uma criança, a partir do momento que o modelo está pronto ele deve acusar se um determinado indivíduo é adulto ou criança.

# Tecnologias utilizadas
O projeto foi contruído no google collab como um arquivo Jupiter Python;
Utiliza majoritariamente funções das bibliotecas:
 - PyTorch Geometric (com alguumas extensões);
 - NetworkX (com algumas extensões);
 - NiLearn;
 - NumPy e ScyPy;
 - MatPlotLib;
 - TQDM;
 - Pandas.

# Principal funcionalidade
Fazer a leitura de dados referentes as atividades cerebrais de alguém e a partir disso montar um grafo
<br/><img width="138" height="67" alt="image" src="https://github.com/user-attachments/assets/94cf2977-7081-425a-b8e8-9688ac3e31ab" /> -> <img width="118" height="166" alt="image" src="https://github.com/user-attachments/assets/54bb5d55-4f8a-43b7-b129-db4aee200221" /><br/>
então percorrer esse grafo com uma GNN e deficir se o cérebro pertence a um adulto ou uma criança



# Requisitos e instruções 
*1. Versão do Python*
  Recomendado: Python >= 3.8 (algumas bibliotecas podem não funcionar com versões mais antigas)
<br/>*2. Bibliotecas Necessárias*
  Abaixo está a lista das bibliotecas utilizadas no código e suas versões recomendadas :
 - torch >=1.10 Deep learning com PyTorch
 - torchvision >=0.11 Pode ser necessário indiretamente
 - torch-geometric (PyG) >=2.0 Processamento de grafos e GNNs
 - numpy >=1.20 Manipulação de arrays
 - matplotlib >=3.4 Visualização de gráficos
 - tqdm >=4.60 Barras de progresso
 - nilearn >=0.9 Processamento de imagens neurocientíficas (fMRI), extração de séries temporais
 - networkx >=2.6 Manipulação de grafos
 - pandas >=1.3 Leitura/escrita de CSV ( labels.csv )
 - scikit-learn >=1.0 Pode ser usado indiretamente por Nilearn
 - scipy >=1.7 Usado pelo Nilearn
<br/>*3. Instalação das Dependências*
Você pode instalar as dependências com os seguintes comandos:
  #Instale o PyTorch conforme sua GPU/CPU:<br/>
  #Para CPU:<br/>
  pip install torch torchvision torchaudio<br/>
  #Para GPU (CUDA compatível), siga instruções em: https://pytorch.org/get-started/locally/ <br/>
  #Instale outras bibliotecas<br/>
  pip install numpy matplotlib tqdm nilearn networkx pandas scikit-learn scipy<br/>
  #A instalação do torch-geometric requer versões compatíveis com o PyTorch instalado. <br/>
  pip install torch-geometric<br/>
<br/>*4. Outras Considerações*
 - O código terá uma estrutura de pastas assim:
dataset/
├── corr_matrices/
├── pcorr_matrices/
├── time_series/
├── labels.csv
└── avg_pcorr.csv
Tome cuidado com qualqer redundância ou adapte o código.
 - Dados Neuroimaging
O código usa nilearn e um atlas. Esses datasets são baixados automaticamente na primeira execução, portanto exigem conexão com internet.
<br/>*5. Compatibilidade com GPU (Opcional)*
 - Ter uma placa NVIDIA compatível com CUDA.
 - Instalar versão CUDA do PyTorch.
 - Verificar compatibilidade entre versões do PyTorch, PyG e CU
A partir desse momento é possível apenas baixar o arquivo .py ou .ipynb no collab e rodar na sua IDE.

# Possíveis melhorias
Testar com outros datasets (ex: Alzheimer, TDAH)
Explorar outras arquiteturas: GAT, GIN, GraphSAGE
Aumentar número de amostras com data augmentation

