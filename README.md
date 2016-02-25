#Dicionário

Seguem os tipos, campos e descrições da ficha do **Produto:**

Coluna/Campo | Tipo/Opções | Descrição
------------ | ------------- |------------ 
Comando | I=Inclusão A=Alteração E=Exclusão | Indica a ação a ser realizada
NomeCat | varchar(25) | Nome da categoria
IDProduto | int | ID  interno do banco de dados

CodProd | varchar(15) | Código de referência do produto, exibido ao visitante

NomeProd | varchar(100) | Nome do produto

Peso | real | Peso do produto. A unidade (gramas ou quilogramas) é definida na página Dados da loja

Descricao | varchar(200) | Descrição curta do produto

DescrLonga | varchar(1024) | Descrição longa do produto

DescrURL | varchar(100) | URL para mais detalhes do produto

URLTarget | bit | Se TRUE, URL do campo DescrURL Será exibida em uma nova janela

Estoque | smallint | Quantidade de itens do produto em estoque

EstoqueMinimo | smallint | Quantidade mínima de itens do produto em estoque. Quando estoque ficar menor, será enviado e-mail para o lojista. Se 0, não tem mínimo.

Disponivel | bit | Se TRUE, produto está disponível no site

ICMS | real | Percentual de ICMS na origem do Produto, para geração de nota fiscal

Custo | money | Custo do produto, nunca exibido ao visitante, utilizado para cálculo nos relatórios de lucratividade.

Preco | money | Preço de venda varejo (B2C)

PrecoProm | money | Preço promocional no varejo (B2C)

PrecoB2B | money | Preço de venda atacado (B2B)

PrecoB2BProm | money | Preço promocional no atacado (B2B)

DataPromInicio | smalldatetime | Data de inicio da promoção, pode-se informar a hora. Ex: 10/05/2002 10:30

DataPromFim | smalldatetime | Data de término da promoção, pode-se informar a hora. Ex: 10/05/2002 10:30

Lancamento | bit | Se TRUE, indica que o produto é lançamento

EmDestaque | bit | Se TRUE, indica que o produto tem destaque no layout da loja. Ver tag <prod>

ImagemProd | varchar(200) | Nome do arquivo com a imagem principal do produto com extensão JPG, PNG, GIF ou SWF

ImagemDet | varchar(200) | Nome do arquivo com a imagem de detalhe do produto com extensão JPG, PNG, GIF ou SWF

ImagemAmp | varchar(200) | Nome do arquivo com a imagem ampliada do produto com extensão JPG, PNG, GIF ou SWF

Adicional1 | varchar(1024) | ID para informação adicional sobre o produto, indicado em Descritor especial 1. Se multivalorado colocar entre vírgulas.

Adicional2 | varchar(1024) | ID para informação adicional sobre o produto, indicado em Descritor especial 2. Se multivalorado colocar entre vírgulas.

Adicional3 | varchar(1024) | ID para informação adicional sobre o produto, indicado em Descritor especial 3. Se multivalorado colocar entre vírgulas.

AdicionalD1 | varchar(2048) | Texto da informação adicional sobre o produto, indicado em Descritor simples 1. Se multivalorado, colocar entre vírgulas.

AdicionalD2 | varchar(2048) | Texto da informação adicional sobre o produto, indicado em Descritor simples 2. Se multivalorado, colocar entre vírgulas.

AdicionalD3 | varchar(2048) | Texto da informação adicional sobre o produto, indicado em Descritor simples 3. Se multivalorado, colocar entre vírgulas.

Cores | varchar(1024) | ID das cores disponíveis no produto. Se multivalorado, colocar entre vírgulas.












