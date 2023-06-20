# Trabalho21_06-IntroCienciaDaComp-
Trabalho do professor Viel de Introdução a ciencia da computação

O código fornecido utiliza a biblioteca OpenCV para realizar uma série de operações morfológicas em imagens em escala de cinza. Essas operações morfológicas são técnicas de processamento de imagem que manipulam a forma e a estrutura dos objetos presentes na imagem.

O código começa lendo três imagens em escala de cinza: 'j.png', 'j_ruido.png' e 'j_furos.png'. Cada imagem é armazenada em uma variável correspondente: "img", "img_opening" e "img_closing", respectivamente.

Em seguida, a altura e a largura da imagem "img" são obtidas e armazenadas nas variáveis "altura" e "largura".

É criado um kernel 5x5 preenchido com uns usando a biblioteca NumPy. O kernel é uma matriz de convolução que será usado nas operações morfológicas.

O conteúdo do kernel é impresso na saída.

A primeira operação morfológica aplicada é a erosão, usando a função `cv2.erode()`. A erosão desgasta as bordas dos objetos presentes na imagem "img". A imagem resultante é armazenada na variável "erosion".

Em seguida, é realizada a operação de dilatação usando a função `cv2.dilate()`. A dilatação expande as áreas brancas presentes na imagem "img". O resultado é armazenado na variável "dilation".

O código também aplica a operação de gradiente morfológico, usando a função `cv2.morphologyEx()`. Essa operação destaca as bordas da imagem, calculando a diferença entre a imagem erodida e a imagem dilatada. O resultado é armazenado na variável "gradient".

Duas outras operações morfológicas são realizadas: abertura e fechamento. A abertura é uma combinação de erosão seguida de dilatação e é usada para remover ruídos e detalhes indesejados na imagem. O resultado da abertura é armazenado na variável "opening". O fechamento, por sua vez, é uma combinação de dilatação seguida de erosão, utilizada para preencher pequenos buracos e fechar pequenas aberturas na imagem. O resultado do fechamento é armazenado na variável "closing".

Por fim, as imagens resultantes das operações morfológicas (erosão, dilatação, abertura, fechamento e gradiente) são exibidas utilizando a função `cv2_imshow()`.

O código apresentado é útil para realizar pré-processamento de imagens, removendo ruídos, destacando bordas e melhorando a qualidade da imagem para posterior análise e extração de informações.
