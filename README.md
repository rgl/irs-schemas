Este repositório contém os schemas utilizados para validar o ficheiro da declaração de [IRS](http://info.portaldasfinancas.gov.pt/pt/informacao_fiscal/codigos_tributarios/irs/index_irs.htm) - Modelo 3.

Estes schemas foram obtidos no [Portal das Finanças](https://www.portaldasfinancas.gov.pt/) através do menu:

  * Serviços Tributários
  * Outros Serviços
  * Formato de Ficheiros

Nomeadamente em [Suporte Informático - Formato de ficheiros](http://www.portaldasfinancas.gov.pt/de/ajuda/DGCI/FAQSI.htm).

**NB** Os ficheiros foram renomeados para refletir o seu ano (e.g. de `Modelo3IRS.xsd` para `Modelo3IRSv2016.xsd`). 

**NB** Os ficheiros sofreram uma pequena alteração de formatação através do [xmllint](http://linux.die.net/man/1/xmllint), e.g.: 

	xmllint --format types.xsd > types.formatted.xsd

Pode-se verificar, com o [diff](http://linux.die.net/man/1/diff), que a alteração apenas modificou os *[whitespaces](http://en.wikipedia.org/wiki/Whitespace_character)* e removeu o [BOM](http://en.wikipedia.org/wiki/Byte_order_mark):

	diff -uwB types.xsd types.formatted.xsd

**NB** Os ficheiros foram também validados pela ferramenta [ValidateSchema](https://github.com/rgl/ValidateSchema/releases).