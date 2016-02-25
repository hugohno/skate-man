#Melhores práticas

Seguem algumas dicas para melhor utilização da API: 

1. Para maximizar a performance na alteração de produtos, inclua no XML somente os campos obrigatórios Comando e IDProduto e os campos que serão alterados. Não inclua no XML campos que não serão alterados. 

2. Existe um limite de até 300 chamadas à API por hora. Cada acesso contabiliza um pageview, independente da quantidade de registros incluídos, alterados ou removidos. Para maximizar o uso de cada chamada aos métodos OrderUpdate e ProductManagement, é possível incluir mais de um registro que será afetado em cada chamada. Por exemplo, é possível incluir, alterar e excluir vários produtos em uma mesma chamada ao método ProductManagement. 

3. Nos métodos UtilityExecute e ReportView, preencha os parâmetros de data sempre que estes existirem no objeto chamado.
Informe sempre o menor período de tempo possível, para maximizar a performance e evitar timeouts. 

4) É possível informar a hora nos parâmetros de data. Se somente a data for informada, sem a hora, esta será considerada 00:00 (meia-noite). 

**Exemplo:** Para obter todos os pedidos do dia 15/09/2011, informe De:15/9/2011 00:00 Até:16/9/2011 00:00 ou, de forma equivalente, De:15/9/2011 Até:16/9/2011.

5. Os relatórios do FastCommerce podem ser acessados via XML, através do método ReportView. Frequentemente incluímos no-vos campos nas dezenas de relatórios do FastCommerce, sem aviso prévio. Por esta razão, os sistemas integrados ao FastCommerce não devem ser afetados por estas inclusões de campos, independente da posição.

Uma programação bem feita de leitura de XML não deve ser "amarrada" com relação à posição do campo, dentro da mesma hierarquia. Se acrescentarmos campos antes ou depois do campo desejado, sem alterar a estrutura do XML, seu programa deve ser capaz de acessar normalmente os nós pré-existentes.

O XML não deve ser lido como uma grande "string". Ao invés disto, seu programa deve manipular o XML como uma estrutura hierárquica, com acesso direto e individualizado a qualquer nó, independente dos nós anteriores e posteriores. Uma sugestão é utilizar objeto para leitura e "parse" do XML, como por exemplo, o Microsoft.XMLDOM, que usamos no FastCommerce.

XML DOM Reference

[http://msdn.microsoft.com/pt-br/library/aa925430.aspx] (http://msdn.microsoft.com/pt-br/library/aa925430.aspx)
