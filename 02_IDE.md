By Rodrigo Esteves de Lima Lopes *University of Campinas* [rll307\@unicamp.br](mailto:rll307@unicamp.br)

------------------------------------------------------------------------
# IDE (Integrated Development Environment)

O R é um software fascinante, mas não traz uma interface muito fácil para seus usuários. Como podemos ver na imagem abaixo, R não é muito amigável:

- Não há realce de sintaxe
- Não há indicação visual do que está na memória do nosso computador
- Não há lugar para escrever nossos scripts e executá-los.

![R em um terminal](./images/R01.png)

Praticamente é uma janela em branco com um cursor e algumas informações técnicas. Existe outra interface, também nativa, que vem com algumas distribuições do R (veja a imagem abaixo), mas é igualmente hostil.

![R numa IDE nativa](./images/R02.png)

É por isso que a maioria dos usuários de R precisa de um *Ambiente de Desenvolvimento Integrado*, ou IDE, para abreviar. Esse tipo de aplicação possibilita aos usuários acessar muitas funções que estão escondidas dentro do R. Outras vantagens são o realce de sintaxe e instalação mais fácil de pacotes e alpem de uma interface mais rica. A interface nos leva a uma navegação mais confortável, pois um 'clique' pode substituir alguns comandos.

Aqui farei uma breve revisão de alguns dos IDEs disponíveis. Durante o nosso workshop, por favor, sinta-se à vontade para usar um que achar melhor.

Observe que o R deve ser instalado antes desta etapa.

## IDEs para codificar

### RStudio

[RStudio](https://rstudio.com/) é um IDE muito poderoso e popular que faz mais do que apenas codificação R (função primária). Também oferece:

- Editor Python
    - Códigos e arquivos Python
- Editor de Markdown
    - Um editor de texto para linguagens de marcação
- Editor Rmarkdown
    - Um editor de texto que permite exportar para vários formatos (HTML, PDF, DOCX etc.)
- Visualização de funções
- Visualização de parcotes e outros resultados
- Visualização de variáveis ​​de dados dentro do IDE
- Gerenciamento de pacotes (instalar, desinstalar, carregar)
- Tutoriais básicos
- Gerenciador de arquivos básico
- Integração Shell (terminal)

![ Exemplo Rstudio](http://mercury.webster.edu/aleshunas/R_learning_infrastructure/images/RStudio%20-%20environment%20panel.png)

A instalação é bem simples, também:

1.  Vá para o site do [RStudio](https://rstudio.com/)
2.  Cliquem produtos/Rstudio
3.  Role a tela para baixo e clique em Rstudio Desktop
4.  Baixe *Open Source Edition* de acordo com seu sistema operacional
    -   Note que nós vamos usar a versão "free"

RStudio é minha IDE preferida. Existe uma comunidade massiva de usuários do RStudio, por favor, acesse o site [RStudio](https://rstudio.com/) para mais informações.

### Pycharm

[PyCharm](https://www.jetbrains.com/pycharm/) é um IDE desenvolvido inicialmente para Python. No entanto, traz [plugin de suporte ao R](https://www.jetbrains.com/help/pycharm/r-plugin-support.html) bem amigável. Ele oferece todas as funções que  há no RStudio, com a pequena diferença de que o [PyCharm](https://www.jetbrains.com/pycharm/) é orientado a bojeto. Isso quer dizer que você tem que criar um projeto e designar um diretório para ele se quiser fazê-lo funcionar. Em termos práticos, isso cria um ambiente virtual que não executa arquivos que não estejam relacionados a um projeto.

![Exemplo de PyCharm](https://resources.jetbrains.com/help/img/idea/2020.2/py_r_overview.png)

A única razão pela qual eu não uso o [PyCharm](https://www.jetbrains.com/pycharm/) regulamente é porque eu tive alguns problemas com o suporte dele ao Rmarkdown.

A instalação também é muito simples:

1.  Vá para o site [PyCharm](https://www.jetbrains.com/pycharm/)
2.  Clique em download
3.  Baixe "community" (free edition)

Depois de instalar o PyCharm, você vai ter que instalar o plug-in da linguagem R language:

1.  Abra o software PyCharm
2.  Abra Settings/Preferences/Plugins
3.  Dê uma busca por "R Language for IntelliJ" e instale-o
4.  Reinicie o PyCharm

Se quiser ver alguns tutoriais específicos:

1.  Plugin PyCharm R [page](https://www.jetbrains.com/help/pycharm/r-plugin-support.html)
2.  Instalação do [Pycharms plugins](https://www.jetbrains.com/help/pycharm/managing-plugins.html)

## IDEs para estudar

Existem alguns IDEs destinados a escrever notebooks. Principalmente para publicação ou para manter notas sobre códigos.

## RStudio

RStudio pode ser útil para criar notebooks para estudo e posterior publicação de código. No entanto, para usar esse recurso, você terá que aprender algumas "markdowns". Markdown é uma linguagem para formatação de texto bastante simples e eficaz. Este tutorial foi escrito em Rmarkdown, uma variedade de markdown aplicada ao R.

Para mais informações sobre o tema:

-   [Rmarkdown web page](https://rmarkdown.rstudio.com/)
-   [R notebooks](https://rmarkdown.rstudio.com/lesson-10.html)

Você verá que o Rmarkdown pode escrever uma série de documentos complexos, usando a mesma plataforma que usamos para pesquisa.

![R Notebook](https://d33wubrfki0l68.cloudfront.net/14588820b42b46fc38e5350566c03420e4c64e34/e54b8/lesson-images/notebooks-1-notebook.png)

### Jupyter notebooks

[Jupyter Notebook](https://jupyter.org/) é um IDE para anotações e publicação de código. Ele funciona como um editor em seu navegador e cria saídas HTML que podem ser úteis para referência pessoal ou mesmo para publicação. Funciona com uma variedade de linguagens de programação.

![Exemplo de Jupyter Notebook](images/binder-50.png)

A instalação do [Jupyter](https://jupyter.org/) é um pouco complexa, mas vale o esforço.

1.  DBaixe e instale a última versão de [Python](https://www.python.org/) para o seu sistema operacional
2.  Abra uma janela de terminal (sim, vamos usá-la)
3.  Execute `Python -m pip install --upgrade`
4.  Execute `pip install jupyterlab`
5.  Execute `jupyter notebook` to start [Jupyter](https://jupyter.org/) for the first time
6.  Abra o RStudio
7.  Crie um novo script digitando as duas linhas abaixo:
    -   `install.packages('IRkernel')` - Installs a package for integration
    -   `IRkernel::installspec(user = FALSE)` - Makes a R Kernel available for Jupiter's system
8.  Volte para o terminal, execute `jupyter notebook` ae já pode começar a usá-lo.
    -   Clique em New/R e obtenha um novo notebook

Um tutorial excelente pode ser achado [aqui](https://dzone.com/articles/using-r-on-jupyternbspnotebook).
