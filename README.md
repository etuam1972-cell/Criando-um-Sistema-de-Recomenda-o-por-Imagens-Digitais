Sistema de Recomendação Visual de Produtos (Image Similarity)
Este projeto implementa um Sistema de Recomendação baseado em Similaridade Visual para e-commerce. Diferente dos sistemas tradicionais que utilizam atributos textuais (como marca, preço ou categoria), esta solução utiliza Deep Learning (Transfer Learning) para extrair a representação vetorial (embeddings) das imagens e recomendar produtos visualmente parecidos em termos de formato, cor, estilo e textura.

📌 Funcionalidades
Extração de Embeddings Visuais: Utiliza o modelo pré-treinado ResNet50 (ImageNet) sem a camada de classificação para extrair vetores numéricos de 2048 dimensões representativos de cada imagem.

Normalização L2: Normaliza os vetores de características para garantir comparações eficientes usando a métrica de distância cosseno.

Armazenamento de Embeddings: Salva a matriz de características e os caminhos das imagens no formato .npy para rápida reutilização sem a necessidade de recomputar a rede neural.

Algoritmo de Busca por Proximidade: Utiliza o k-Nearest Neighbors (k-NN) com distância cosseno para indexar e encontrar rapidamente os produtos mais similares a uma imagem de consulta (query).

Visualização de Resultados: Exibe graficamente o produto selecionado/buscado ao lado dos produtos recomendados utilizando Matplotlib.
