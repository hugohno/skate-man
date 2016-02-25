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

Seguem os tipos, campos e descrições da ficha do **Clientes:**

Coluna/Campo | Tipo/Opções | Descrição
------------ | ------------- |------------ 
Cadastro em | smalldatetime | Indica a data de cadastramento do cliente
Tipo | Opções: PF ou PJ | Indica se o cliente é pessoa física ou jurídica
Empresa | varchar(50) | Nome da empresa, somente quando B2B
Contato | varchar(50) | Nome
E-mail | varchar(50) | E-mail
CNPJ/CPF | varchar(14) | CPF ou CNPJ
IE/RG | varchar(20) | Inscrição estadual ou RG
Ramo | varchar(30) | Profissão do cliente ou ramo de atuação da empresa
% Desc | real | Percentual de desconto global nos produtos para o cliente. 
Endereço | varchar(70) | Endereço
Bairro | varchar(25) | Bairro
Cidade | varchar(20) | Cidade
Estado | char(2) | Estado
País | varchar(20) | País
CEP  |varchar(9) | CEP
Telefone | varchar(20) | Telefone
FAX | varchar(20) | FAX
Obs curta | varchar(10) | Texto de apoio sobre o cliente, para uso interno da loja.
Data Nasc | smalldatetime | Data de nascimento
Pagtos | varchar(80) | Indica as formas de pagamento que este cliente pode utilizar, quando a loja tem formas de pagamento por cliente.
Sexo | Opções: PF ou PJ | Sexo do cliente
Última alteração | smalldatetime | Data/hora da última alteração do cliente
Logradouro | varchar(70) | Endereço do cliente
Endereço número | varchar(70) | Número do endereço
Endereço complemento | varchar(70) | Complemento do endereço
Celular | varchar(20) | Telefone móvel completo para contato e envio SMS (com DDD)
Campo 1 | varchar(100) | Campo adicional 1
Campo 2 | varchar(100) | Campo adicional 2
Campo 3 | varchar(100) | Campo adicional 3

Seguem os tipos, campos e descrições da ficha do **Pedidos:**

Coluna/Campo | Tipo/Opções | Descrição
------------ | ------------- |------------ 
Nome Cliente | varchar(50) | Nome do cliente
E-mail | Cliente varchar(50) | E-mail do cliente
Telefone | varchar(20) | Telefone do cliente
Cidade | varchar(20) | Cidade do cliente
Estado | char(2) \ Estado do cliente
Núm Pedido | int | Número do pedido
Produto(s) do Pedido | varchar(100) | Nome do produto
Ref. | varchar(15) | Referência do produto
Qtd | smallint | Quantidade de itens do produto
Total sem frete | money | Valor total do pedido, SEM o frete
Frete | money | Valor do frete
Total com frete | money | Valor total do pedido, COM o frete
Pagamento | varchar(50) | Opção de pagamento escolhida pelo cliente
Cartão | Opções: AMEX, Diners, Mastercard, VISA, Hipercard, Aura e Elo | Bandeira de cartão de crédito
Status | opções: Novo, Cancelado, em aprovação, Pendente, Aprovado, Liberado e Remetido | Status do pedido
Feito em | smalldatetime | Data em que o pedido foi feito
Obs curta | varchar(10) | Texto de apoio sobre o pedido, para uso interno da loja
Entregue Em | smalldatetime | Data de entrega do pedido ao destinatário pela transportadora
Objeto SEDEX | varchar(13) | Código fornecido pelos Correios para acompanhamento de remessas
MoipCodigo | varchar(12) | Código da transação retornada pelo MoIP. Ex: 11202666
MoipStatus | tinyint | Status da transação retornada pelo MoIP. Ex: 5 Os valores possíveis para o campo MoipStatus: (1) Autorizado: Pagamento autorizado. (2) Iniciado: Pagamento foi iniciado, porém sem confirmação de finalização até o momento (3) BoletoImpresso: Boleto visualizado pelo cliente (4) Concluído: Pagamento creditado em conta e disponível para saque. (5) Cancelado: Pagamento foi cancelado (6) EmAnalise: Pagamento em análise de risco (7) Estornado: Pagamento foi estornado (8) EmRevisao: Pagamento em revisão pelo Moip (9)  Reembolsado: Pagamento foi reembolsado
AkatusID | varchar(36) | O ID da transação na Akatus. Ex: cfbda716-906b-4f69-83f8-4cdae19cb3ee
AkatusStatus | varchar(50) | Status da transação na Akatus. Ex: Cancelado Os valores possíveis para o campo AkatusStatus: Aguardando Pagamento, Em Análise, Aprovado e Cancelado.
ChangeFlagAPI | tinyint | Utilizado para marcar os pedidos que já foram recebidos pelo ERP, evitando que sejam novamente trazidos.

Seguem os tipos, campos e descrições da ficha do **Detalhes:**

Coluna/Campo | Tipo/Opções | Descrição
------------ | ------------- |------------ 
Núm | int | Número do pedido
Feito em | smalldatetime | Data em que o pedido foi feito
Nome | varchar(50) | Nome do cliente
E-mail | varchar(50) | E-mail do cliente
Empresa | varchar(50) | Nome da empresa, somente quando B2B
CPF/CNPJ | varchar(14) | CPF ou CNPJ
RG/IE | varchar(20) | Inscrição estadual ou RG
Endereço | varchar(70) | Endereço
Bairro | varchar(25) | Bairro
Cidade | varchar(20) | Cidade
Estado | char(2) | Estado
País | varchar(20) | País
CEP | varchar(9) | CEP
Telefone | varchar(20) | Telefone
FAX | varchar(20) | FAX
Nascido em | smalldatetime | Data de nascimento
Obs cliente | varchar(10) | Texto de apoio sobre o cliente, para uso interno da loja.
Nome Pedido | varchar(50) | Nome para entrega do pedido
E-mail Pedido | varchar(50) | E-mail para entrega do pedido
Endereço Pedido | varchar(70) | Endereço de entrega
Bairro Pedido | varchar(25) | Bairro de entrega
Cidade Pedido | varchar(20) | Cidade de entrega
Estado Pedido | char(2) | Estado de entrega
País Pedido | varchar(20) | País de entrega
CEP Pedido | varchar(9) | CEP de entrega
Telefone Pedido | varchar(20) | Telefone de entrega
FAX Pedido | varchar(20) | FAX de entrega
Total sem frete | money | Valor total do pedido, SEM o frete
Frete | money | Valor do frete
Pagamento | varchar(50) | Opção de pagamento escolhida pelo cliente
Cartão | Opções: AMEX, Diners, Mastercard, VISA, Hipercard, Aura e Elo | Bandeira de cartão de crédito
Parcelas | tinyint | Número de parcelas
Presente | opções: S ou N | Se é para presente
Status | opções: Novo, Cancelado, em aprovação, Pendente, Aprovado, Liberado e Remetido |Status do pedido
Obs Pedido | varchar(10) | Texto de apoio sobre o pedido, para uso interno da loja
Entregue em | smalldatetime | Data de entrega do pedido ao destinatário pela transportadora
Obj SEDEX | varchar(13) | Código fornecido pelos Correios para acompanhamento de remessas
Ref. Produto | varchar(15) | Referência do produto
Nome Produto | varchar(100) | Nome do produto
Qtd | smallint | Quantidade de itens do produto
Preço unit | money | Preço unitário do produto
Msg cliente | varchar(255) | Comentários feitos pelo cliente
Local de entrega | varchar(50) | Local de entrega do pedido
Parceiro | varchar(30) | Quando o pedido foi feito através de um parceiro, informa o nome do parceiro
ThisfTransacao | varchar(14) | Código de transação com cartão de crédito recebido da Thisf, se a loja utiliza
Esp1 | varchar(30) | Informação adicional sobre o produto, indicado em Descritor especial 1
Esp2 | varchar(30) | Informação adicional sobre o produto, indicado em Descritor especial 2
Esp3 | varchar(30) | Informação adicional sobre o produto, indicado em Descritor especial 3
Simp1 | varchar(30) | Informação adicional sobre o produto, indicado em Descritor simples 1
Simp2 | varchar(30) | Informação adicional sobre o produto, indicado em Descritor simples 2
Simp3 | varchar(30) | Informação adicional sobre o produto, indicado em Descritor simples 3
DescontoTotalSF | real | Desconto em % aplicado no total do pedido SEM o frete
IDProduto | int | ID interno do produto no banco de dados
Valor embalagem | smallmoney | Valor para a embalagem de presente
Cor | varchar(30) | Cor solicitada do produto
Cod. barras | varchar(25) | Código de barras do produto
ObsCurta | varchar(10) | Campo para informar um pequeno texto de observação do pedido
ccNum | varchar(19) | Número do cartão de crédito
ccNome | varchar(30) | Nome gravado no cartão de crédito
ccSeg | varchar(4) | Código de segurança do cartão de crédito
ccDataExp | varchar(7) | Mês/Ano em que o cartão expira (Ex: 05/2001)
ccAuthCod | varchar(10) | Autorização da administradora do cartão
ccNumCV | varchar(9) | Número do comprovante de venda, emitido pela administradora do cartão
ccNumAutent | varchar(27) | Número de autenticação da venda, emitido pela administradora do cartão
ccNumPrg | varchar(1) | Retorno do Komerci SecureCode (0,1,2,3,4)
ccCodRet | varchar(2) | Código de retorno do processo de autorização da venda, informado pela administradora do cartão
ccORIGEM_BIN | char(3) | Cód país emissor Komerci
ccEndereco | varchar(100) | Endereço reportado pela Redecard via AVS
VisaTID | char(20) | Identificação da transação na Cielo
VisaLR | varchar(4) | Cód de retorno da Cielo
VisaARP | varchar(6) | Cód aprovação bancária informado pela Cielo, somente para pedidos autorizados.
VisaCOD | varchar(4) | Código do resultado da captura do pedido informado pela Cielo
VisaAuth | varchar(3) | Indica se o pedido foi autenticado pelo banco emissor: 0 ou vazio=transação sem autenticação 1=ok 2=negado 3=falha
VisaCAP | money | Valor capturado informado pela Cielo
VisaBank | varchar(4) | Código do banco emissor do cartão
ThisfAutorizacao | varchar(6) | Código de autorização recebido pela Thisf da administradora do cartão
MoipCodigo | varchar(12) | Código da transação retornada pelo MoIP
MoipStatus | tinyint | Status da transação retornada pelo MoIP
AkatusID | varchar(36) | O ID da transação na Akatus.
AkatusStatus | varchar(50) | Status da transação na Akatus
Tipo | Opções: PF ou PJ | Indica se o cliente é pessoa física ou jurídica
Logradouro | varchar(70) | Endereço do cliente
Endereço número | varchar(70) | Número do endereço
Endereço complemento | varchar(70) | Complemento do endereço
Celular | varchar(20) | Telefone móvel completo para contato e envio SMS (com DDD)
Campo 1 | varchar(100) | Campo adicional 1
Campo 2 | varchar(100) | Campo adicional 2
Campo 3 | varchar(100) | Campo adicional 3
Logradouro Pedido | varchar(70) | Endereço
Endereço número Pedido | varchar(70) | Número do endereço
Endereço complemento Pedido | varchar(70) | Complemento do endereço
Campo 1 Pedido | varchar(100) | Campo adicional no pedido 1
Campo 2 Pedido | varchar(100) | Campo adicional no pedido 2
Campo 3 Pedido | varchar(100) | Campo adicional no pedido 3
ThisfAutorizacao | varchar(6) | Código de autorização recebido pela Thisf da administradora do cartão
Embalar Produto | Opções: S ou N | Indica se produto deve ser embalado
Valor embalagem produto | smallmoney | Valor para embalagem do produto
Desconto Cupom | real | Valor em $ do desconto no pedido
ChangeFlagAPI | tinyint | Utilizado para marcar os pedidos que já foram recebidos pelo ERP, evitando que sejam novamente trazidos.
Alterado em | smalldatetime | Data da última alteração do pedido
Logradouro | varchar(70) | Endereço do cliente

Seguem os tipos, campos e descrições da ficha de **Acessos:**

Coluna/Campo | Tipo/Opções | Descrição
------------ | ------------- |------------ 
Method | Opções: ReportView, OrderUpdate, ProductManagement, NfeOperation, UtilityExecute. | Indica o método
Nome | varchar(80) | Indica o nome do relatório, utilitário.
Data execução | datetime | Data/hora de início do processamento
Usuário | varchar(20) | Nome do usuário
Regs | int | Quantidade de registros lidos, incluídos, alterados ou excluídos
Parâm 1 | varchar(15) | Legenda para o parâmetro 1
Valor 1 | varchar(100) | Valor informado no parâmetro 1
Parâm 2 | varchar(15) | Legenda para o parâmetro 2
Valor 2 | varchar(100) | Valor informado no parâmetro 2
Parâm 3 | varchar(15) | Legenda para o parâmetro 3
Valor 3 | varchar(100) | Valor informado no parâmetro 3
Parâm 4 | varchar(15) | Legenda para o parâmetro 4
Valor 4 | varchar(100) | Valor informado no parâmetro 4
Parâm 5 | varchar(15) | Legenda para o parâmetro 5
Valor 5 | varchar(100) | Valor informado no parâmetro 5
Parâm 6 | varchar(15) | Legenda para o parâmetro 6
Valor 6 | varchar(100) | Valor informado no parâmetro 6
Parâm 7 | varchar(15) | Legenda para o parâmetro 7
Valor 7 | varchar(100) | Valor informado no parâmetro 7
Parâm 8 | varchar(15) | Legenda para o parâmetro 8
Valor 8 | varchar(100) | Valor informado no parâmetro 8
