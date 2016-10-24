# Template Mestrado PROCC
Template desenvolvido **independentemente** para o arquivo em formato PDF contendo toda a documentação necessária para o ingresso no mestrado em computação da Universidade Federal de Sergipe.

O comando ``pdffile`` utilizado no template foi criado (``\newcommand``) para auxiliar na inclusão de PDFs no documento. Este comando utiliza o package PDFPages (https://www.ctan.org/pkg/pdfpages) e deve ser utilizado da seguinte forma:

``\pdffile{arg1}{arg2}{arg3}{arg4}``

Os argumentos requeridos são os seguintes:

* arg1 (boolean): true se o pdf a ser incluido possui mais de uma página, false caso contrário. Este campo é na verdade uma string, então qualquer valor diferente de "false" (case sensitive) será interpretado com verdadeiro. 
* arg2 (float): escala do pdf a ser incluido. Normalmente uma escala entre 0.75 e 0.9 é suficiente para ajustar o documento à pagina.
* arg3 (string): comandos LaTeX a serem inseridos antes do pdf. Utilize normalmente comandos para iniciar a seção, visto que, caso o comando \section{title} seja utilizado antes do comando \pdffile, haverá uma quebra de página antes da inserção do pdf. Para não utilizar nenhum comando, basta colocar chaves, ex: \pdffile{false}{0.75}{{}}{pdf-sem-titulo.pdf}.
* arg4 (string): path do documento pdf a ser incluido. É possível utilizar imagens também, especificando obrigatoriamente a extensão, ex: \pdffile{false}{0.9}{\section{Imagem}}{foto.jpg}.

O comando ``pdffile`` está definido no arquivo ``meta.tex`` e pode ser alterado livremente.
