---
title: "Como salvar imagens em alta resolução no PowerPoint"
date: 2020-05-31
tags: [Gráficos, PowerPoint, HD, dpi]
classes: wide
header:
  image: "/images/header.jpg"
  teaser: /images/publications/TOC_1.png
  og_image: /images/publications/TOC_2.png
excerpt: "Test 1, 2, 3"
mathjax: "true"
---

Por padrão, quando você salva um slide do PowerPoint como imagem ela é salva com uma resolução de 96 DPI. Entretanto, para gerar imagens para publicação ou impressão a maioria das editoras pede por imagens que apresentem 300 DPI ou sejam em formato vetorial. Nesse pequeno tutorial irei ensinar como alterar a resolução padrão de salvamento de imagens do PowerPoint (por incrível que pareça não é algo que pode ser mudado nas opções do programa), além de discutir um pouco os formatos de imagem.

> DPI, ou *dots per inch* em inglês, é uma medida do número de pontos individuais que existem em uma polegada linear na superfície. Em geral é diretamente relacionada à resolução de uma imagem. De maneira geral, quanto maior o número de pontos por polegada, mais bem definida e detalhada é a imagem (e também mais pesada).

# 1° Etapa: Alterando as configurações no registro do windows

Antes de começar é preciso deixar bem claro que iremos alterar as entradas de registro do windows. E apesar de ser um processo simples e que dificilmente você irá fazer algo errado, é importante ter cuidado para não alterar nada mais do que o necessário pois isso pode causar impactos no funcionamento do seu windows. **Mas fique tranquilo, é mais fácil errar um miojo do que errar algum passo desse tutorial.**

1. Abrindo o editor de registros

Para abrir o editor de registros basta clicar na barra de pesquisa do iniciar e pesquisar por **Editor do Registro**. Em seguida clique em abrir, como mostrado na imagem abaixo.

<img src="{{ site.url }}{{ site.baseurl }}/images/posts/graficos/dpi/dpi1.png" alt="Abrindo o Editor do Registro">

Caso você esteja utilizando uma versão antiga do windows, basta clicar em Iniciar > Executar, em seguida digitar regedit e clicar em `OK`.

2. Editando a chave de registro

Agora você precisa localizar a chave de registro da resolução de exportar imagens do PowerPoint. Dependendo da versão do Office que você estiver utilizando, o caminho para essa chave irá ser um pouco diferente:

PowerPoint 2016
HKEY_CURRENT_USER\Software\Microsoft\Office\16.0\PowerPoint\Options

PowerPoint 2013
HKEY_CURRENT_USER\Software\Microsoft\Office\15.0\PowerPoint\Options

PowerPoint 2010
HKEY_CURRENT_USER\Software\Microsoft\Office\14.0\PowerPoint\Options

PowerPoint 2007
HKEY_CURRENT_USER\Software\Microsoft\Office\12.0\PowerPoint\Options

PowerPoint 2003
HKEY_CURRENT_USER\Software\Microsoft\Office\11.0\PowerPoint\Options

Para localizar o caminho, basta ir clicando nos símbolos `>` da respectiva pasta, como mostrado na imagem abaixo.
<img src="{{ site.url }}{{ site.baseurl }}/images/posts/graficos/dpi/dpi2.png" alt="Abrindo o Editor do Registro">

No fim, você deverá estar em uma tela semelhante a essa:
<img src="{{ site.url }}{{ site.baseurl }}/images/posts/graficos/dpi/dpi3.png" alt="Abrindo o Editor do Registro">

Em seguida, clique com o botão direito na subchave **Opções**, aponte para **Novo** e clique em **Valor DWORD**.

<img src="{{ site.url }}{{ site.baseurl }}/images/posts/graficos/dpi/dpi4.png" alt="Abrindo o Editor do Registro">

Digite ExportBitmapResolution e precione `Enter`. Em seguida, selecione a chave ExportBitmapResolution, clique com o botão direito nela e selecione **Modificar**.

<img src="{{ site.url }}{{ site.baseurl }}/images/posts/graficos/dpi/dpi5.png" alt="Abrindo o Editor do Registro">

Selecione a opção `Decimal` no menu **Base** e digite o valor de DPI da imagem que desejar na caixa de **Dados do valor**. Em geral 300 é um bom valor. Caso queira imagens ainda melhores pode colocar 600 ou valores maiores. Não ir muito além disso, a não ser que seja absolutamente necessário, pois as imagens podem ficar muito pesadas e algumas versões mais antigas do PowerPoint podem apresentar erros em salvar imagens tão grandes.

<img src="{{ site.url }}{{ site.baseurl }}/images/posts/graficos/dpi/dpi6.png" alt="Abrindo o Editor do Registro">

Por fim, basta clicar em `OK` e fechar a janela do Editor do Registro.

3. Exportanto slides como imagens

No PowerPoint, abra a apresentação e selecione o slide que deseja exportar. No menu **Arquivo**, selecione **Salvar como**.

Na caixa **Salvar como tipo**, selecione o formato de imagem desejado:

- Formato PNG (\*.png)
- Formato TIFF (\*.tif)
- Formato JPEG (\*.jpg)
- Bitmap Independente de Dispositivo (\*.bmp)

Caso queira enviar esse arquivo para impressão ou algo relacionado, como um artigo ou pôster, recomendo salvar em formato TIFF. Caso queira utilizar essa imagem em uma aplicação digital, como apresentação ou publicação na internet, recomendo utilizar o formato PNG. Só salve em formato .bmp caso seja realmente necessário (o editor peça ou algo assim).

**Nunca, jamais, em hipótese alguma utilize JPEG.**

Após clicar em `Salvar`, você pode escolher a opção **Somente o Slide Atual**, que como o nome diz irá somente salvar o slide que você selecionou, ou a opção **Todos os Slides**, que irá criar uma pasta com o nome que você digitou para salvar e dentro dessa pasta irá salvar todos os slides como imagens independentes.
