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
MoipStatus | tinyint | Status da transação retornada pelo MoIP. Ex: 5 Os valores possíveis para o campo MoipStatus: (1) Autorizado: Pagamento autorizado.-(2) Iniciado: Pagamento foi iniciado, porém sem confirmação de finalização até o momento (3) BoletoImpresso: Boleto visualizado pelo cliente (4) Concluído: Pagamento creditado em conta e disponível para saque. (5) Cancelado: Pagamento foi cancelado (6) EmAnalise: Pagamento em análise de risco (7) Estornado: Pagamento foi estornado (8) EmRevisao: Pagamento em revisão pelo Moip (9)  Reembolsado: Pagamento foi reembolsado
AkatusID | varchar(36) | O ID da transação na Akatus. Ex: cfbda716-906b-4f69-83f8-4cdae19cb3ee
AkatusStatus | varchar(50) | Status da transação na Akatus. Ex: Cancelado Os valores possíveis para o campo AkatusStatus: Aguardando Pagamento, Em Análise, Aprovado e Cancelado.
ChangeFlagAPI | tinyint | Utilizado para marcar os pedidos que já foram recebidos pelo ERP, evitando que sejam novamente trazidos.
