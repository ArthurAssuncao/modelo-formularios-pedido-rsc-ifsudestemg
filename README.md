# MODELO DE FORMULARIOS DE PEDIDO DE RSCs PARA O IF SUDESTE MG

O presente modelo foi baseado no arquivo: "3. FORMULÁRIOS PEDIDO RCS.doc" localizado em:
http://www.ifsudestemg.edu.br/sites/default/files/3.%20FORMUL%C3%81RIOS%20PEDIDO%20RCS.doc


Este modelo em Tex foi desenvolvido por **Arthur Nascimento Assuncao**, servidor do **campus Santos Dumont**.

## Modelo em PDF
https://github.com/ArthurAssuncao/modelo-formularios-pedido-rsc-ifsudestemg/blob/master/rsc.pdf

## Download do modelo
https://github.com/ArthurAssuncao/modelo-formularios-pedido-rsc-ifsudestemg/archive/master.zip

## Instalação

### Instalação no Windows

#### Baixe o TexLive (preferível) ou MikTex
[TexLive - Baixe o install-tl-windows.exe](http://tug.org/texlive/acquire-netinstall.html)

[MikTex - Baixe o Basic MiKTeX Installer ou MiKTeX Net Installer e também o MiKTeX Setup Utility](https://miktex.org/download)

#### Baixe o editor Tex, o TexStudio
[TexStudio](http://texstudio.sourceforge.net/#download)

### Instalação do Tex e TexStudio no Linux
Execute no terminal o seguinte comando:
```tex
# apt-get install texlive-latex-base texlive-latex-extra texlive-bibtex-extra texlive-fonts-recommended texlive-lang-portuguese texstudio
```

## Motivação
Facilitar o preenchimento do pedido, automatizando algumas tarefas e evitando preenchimento não-digital, permitindo assim: 

* Preenchimento automático das informações do servidor e da sua pontuação com base em um arquivo separado (rsc-dados.tex).
* Inclusão de certificados com indicação da pontuação no topo da página (e.g. \incluirpdf{-}{0}{RSC I - 11}{pdfs/certificado.pdf}).
* Páginação com números romanos para seções e arábico dentro das seções (e.g. vi.2).
* Marcação de intervalo de seção (e.g. Relatório descritivo: v.1 até v.8).
* Permitir a referenciação do intervalo de páginas dos certificados (e.g. O certificado de curso de ingês se encontra nas páginas \paginainicialpdf{pdfs/certificado.pdf} até \paginafinalpdf{pdfs/certificado.pdf} gera: [...] nas páginas vii.2 até vii.3).
* Além de fornecer um modelo exato, independente de software (MS Office, libreoffice etc).


## Como usar:
* Os arquivos localizados no diretório "nao-editar" não precisam ser modificados.
* Preencha o arquivo "rsc-dados.tex" com os seus dados e não se esqueça de descomentar (tirar o % do início da linha do "rsc-dados.tex") o comando \removercomentarios{} quando finalizar o preenchimendo do modelo.
* Adicionar o pdf da planilha de simulação no arquivo com o nome "planilha.pdf" (ao gerar o PDF, remova o rodapé [formatar > página > rodapé > ativar rodapé], pois o modelo já inclui a indicação de página no rodapé das páginas). Configure a impressão para remover a primeira planilha do arquivo e para não cortar as tabelas da planilha (Configure isso em visualizar impressão);
  * rsc-planilha-simulacao.tex
* Preencha os arquivos do Relatório Descritivo indicados abaixo:
  * rsc-descricao-itinerario-formacao-titulacao.tex
  * rsc-descricao-atuacao-docente.tex
  * rsc-indicacao-descricao-producao-academica.tex
  * rsc-descricao-atividades-prestacao-servico.tex
  * rsc-indicacao-descricao-atividade-administracao.tex
  * rsc-indicacao-titulos-premios-aprovacoes.tex
* Você pode usar o seguinte exemplo para cada descrição, incluindo colocar uma tabela indicando o RSC e as páginas do certificado:
```tex
2016 - Curso de Latex realizado no IF Sudeste MG, campus Santos Dumont. Documento Comprobatório: certificado.

\addtabelaindicacaocomprovante{RSC I}{I}{4}{\pageref{documentacao-probatoria-rsc-i}.\paginainicialpdf{pdf/certificado.pdf} a \pageref{documentacao-probatoria-rsc-i}.\paginafinalpdf{pdf/certificado.pdf}}
```
* Em seguida adicione os PDFs ou imagens dos seus comprovantes utilizando o comando:
```tex

\incluirpdf{-}{0}{RSC I - 11}{certificado.pdf}
```
* Onde:
  * {-} numero ou numeros de paginas, '-' para incluir todas as páginas.
  * {0} angulo do certificado, 0 para não alterar, 90 para rotacionar 90° para direita.
  * {RSC I - 11} indicação da pontuação do RSC do comprovante.
  * {certificado.pdf} caminho do pdf/jpg/etc do comprovante.
* Seus comprovantes (comando \incluirpdf para cada comprovante) devem ficar nos arquivos abaixo:
  * rsc-documentacao-probatoria-formacao-comprovantes.tex
  * rsc-documentacao-probatoria-rsc-i-comprovantes.tex
  * rsc-documentacao-probatoria-rsc-ii-comprovantes.tex
  * rsc-documentacao-probatoria-rsc-iii-comprovantes.tex
* Gere o PDF e pronto!
* Deu erro em algum pacote? Use um dos pacotes que tem na pasta "sty", basta copiar o arquivo para a pasta raiz ou mudar o usepackage, exemplo:
```tex
\usepackage{tocloft}
para
\usepackage{sty/tocloft}
```
* Gere o PDF de novo e pronto. Finalmente!!!


Mais informações sobre o processo de pedido de RSCs em:

http://www.ifsudestemg.edu.br/institucional/docs

