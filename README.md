# MODELO DE FORMULARIOS DE PEDIDO DE RSCs PARA O IF SUDESTE MG

O presente modelo foi baseado no arquivo: "3. FORMULÁRIOS PEDIDO RCS.doc" localizado em:
http://www.ifsudestemg.edu.br/sites/default/files/3.%20FORMUL%C3%81RIOS%20PEDIDO%20RCS.doc


Este modelo em Tex foi desenvolvido por **Arthur Nascimento Assuncao**, servidor do **campus Santos Dumont**.


## Motivação
A motivação foi facilitar o preenchimento do pedido, automatizando algumas tarefas e evitar preenchimento não-digital, como: 

* Preenchimento automático das informações do servidor com base em um arquivo separado (rsc-dados.tex)
* Inclusão de certificados com indicação da pontuação no topo da página (e.g. \incluirpdf{-}{RSC I - 11}{pdfs/certificado.pdf})
* Páginação com números romanos para seções e arábico dentro das seções (e.g. vi.2)
* Marcação de intervalo de seção (e.g. Relatório descritivo: v.1 até v.8)
* Permitir a referenciação do intervalo de páginas dos certificados (e.g. O certificado de curso de ingês se encontra nas páginas \paginainicialpdf{pdfs/certificado.pdf} até \paginafinalpdf{pdfs/certificado.pdf} gera: [...] nas páginas vii.2 até vii.3)
* Além de fornecer um modelo exato, independente de software (MS Office, libreoffice etc).


## Como usar:
* Os arquivos localizados no diretório "nao-editar" não precisam ser modificados
* Preencha o arquivo "rsc-dados.tex" com os seus dados.
* Preencha os arquivos do Relatório Descritivo indicados abaixo:
* * rsc-descricao-itinerario-formacao-titulacao
* * rsc-descricao-atuacao-docente
* * rsc-indicacao-descricao-producao-academica
* * rsc-descricao-atividades-prestacao-servico
* * rsc-indicacao-descricao-atividade-administracao
* * rsc-indicacao-titulos-premios-aprovacoes
* Em seguida adicione os PDFs ou imagens dos seus comprovantes utilizando o comando:
* * \incluirpdf{-}{RSC I - 11}{certificado.pdf} onde:
* * {-} numero ou numeros de paginas, '-' para incluir todas as páginas
* * {RSC I - 11} indicação da pontuação do RSC do comprovante
* * {certificado.pdf} caminho do pdf/jpg/etc do comprovante
* Seus comprovantes (comando \incluirpdf para cada comprovante) devem ficar nos arquivos abaixo:
* * rsc-documentacao-probatoria-formacao-comprovantes
* * rsc-documentacao-probatoria-rsc-i-comprovantes
* * rsc-documentacao-probatoria-rsc-ii-comprovantes
* * rsc-documentacao-probatoria-rsc-iii-comprovantes
* Gere o PDF e pronto!