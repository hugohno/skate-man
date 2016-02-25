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
OrdemProd | tinyint | Indica a ordem de exibição do produto. Ordenação decrescente.
IDProdutoPai | int | Se preenchido, indica que este é um sub-produto e qual o ID do produto Pai
RamoProd | tinyint | Indica o departamento no Shopping Virtuose.
MaisProd | varchar(50) | Indica termos de busca para produtos relacionados a estes entre vírgula. (cross-selling)
DataVencimento | smalldatetime | Indica a data de vencimento do produto, Quando será enviado e-mail de alerta ao lojista
DiasAvisoVencimento | smallint | Números de dias antes do vencimento do produto, quando será enviado o primeiro e-mail de alerta para o lojista
DiasReposicao | smallint | Número de dias, em média em que o produto é novamente adquirido pelo cliente. Decorridos estes dias após o pedido, um e-mail será enviado ao cliente para sugerir a reposição.
IDParceiroProd | int | Informe o ID do parceiro que terá exclusividade para o preço promocionaldo produto. Desta forma, é possível criar promoções válidas somente paravisitantes cujo acesso seja proveniente de um parceiro ou revendedor específico.
MaxParcelasProd | tinyint | Número máximo de parcelas para pedidos que incluam este produto.
IDCategoria | int | ID interno da categoria cadastrada. No CSV de produtos, ao incluir um produto, é obrigatório o campo NomeCat (com o nome da categoria do produto), o sistema inclui o produto e cria a categoria caso ela não exista. Na API, ao incluir produtos na loja, o campo NomeCat ou IDCategoria deve ser informado. Se a categoria for existente pode ser informado o IDCategoria, sem passar o NomeCat.
XMLParcelasProd | tinyint | Infica o número de parcelas utilizadas para exibir o parcelamento na página que lista os produtos em XML (XMLProdutos.asp). A lista de produtos em XML é utilizado pelos portais de comparação de preços e shopping virtuais, para capturar os produtos da loja. 
Embalavel | bit | Se TRUE, indica o cliente pode solicitar que este produto seja embalado para presente. Deve-se informar FALSE nos produtos que não poderão ser embalados para presente devido ao seu tamanho (exemplo:bicicleta) ou por alguma outra restrição. Este campo é utilizado se a loja utilizar as opções (4), (5) ou (6) no campo "Presente" da página "Envio & frete" do site administrativo onde o cliente tem a opção de informar quais produtos do pedido deseja embalar para presente.
DescrHTM | varchar(25) | Indica o nome do arquivo HTML contendo descrição adicional do produto. O conteúdo do arquivo HTM será incluído na posição da tag especial <DescrHTM>, caso esta tag exista no arquivo personalizado de exibição do layout de produtos na loja (EstiloProduto.htm) 
MetaKeywordsProd | varchar(200) | Palavras-chave (keywords) específicas para o produto. Os termos devemser separados por vírgula. Exemplo: nokia,celular com wi-fi,mp3,rede 3G,GPSSão inseridas em "meta tag keyword", no código fonte da loja.  
CodBarrasProd | varchar(25) | Código de barras do produto
ChangeFlagProdAPI | tinyint | Utilizado para marcar os produtos que já foram recebidos pelo ERP, evitando que sejam novamente trazidos. Veja mais detalhes na seção 3.1. 
IsProdutoGrande | bit | Indica se o produto é considerado grande para cálculo de frete, usando peso cúbico e tabela para frete grande.
DataProdAlteracao | smalldatetime | Data/hora da última alteração do produto (exceto o cancelamento e descancelamento de pedidos)
IDRamo | int | Indica o ID do ramo
NomeRamo | varchar(80) | Nome do Ramo. Ex: Beleza & Saúde, Bermuda Infantil, Bonecos e Personagens, etc.
IDRamoPai | int | Indica o ID do ramo Pai, nulo se for o primeiro nível
IDCategoria | int | ID interno do banco de dados
Categoria | varchar(25) | varchar(25)
Ordem | tinyint | Indica a ordem de exibição. Ordenação decrescente.
IDCategoriaPai | int | Se preenchido, indica que esta é uma sub-categoria e qual o ID da categoria Pai.
Prods | real | Quantidade de produtos

Seguem os tipos, campos e descrições da ficha do Clientes:
