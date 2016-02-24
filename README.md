# XML de pedidos

Estrutura do XML com todos os campos que podem ser alterados na ficha do pedido.

```
<Records>

 <Record>

 <Field Name="NumPedido" Value="999999" />

 <Field Name="ObsCurta" Value="abcdefg" />

 <Field Name="Status" Value="3" />

 <Field Name="ObjSedex" Value="a9b9c9d9e9" />

 <Field Name="ChangeFlagAPI" Value="98" />

 </Record>

 <Record>

 <Field Name="NumPedido" Value="888888" />

 <Field Name="ObsCurta" Value="ijlmopq" />

 <Field Name="Status" Value="1" />

 <Field Name="ObjSedex" Value="a8b8c8d8e8" />

 <Field Name="ChangeFlagAPI" Value="99" />

 </Record>

</Records>
```

Obs: É possível enviar multiplos pedidos por vez.

##4.1 Alteração de pedidos

Estrutura do XML para alteração na ficha dos pedidos: (para alteração, o campo NumPedido é obrigatório)

```
<Records>

 <Record>

 <Field Name="NumPedido" Value="999999" />

 <Field Name="ObsCurta" Value="abcdefg" />

 <Field Name="Status" Value="4" />

 <Field Name="ObjSedex" Value="a9b9c9d9e9" />

 <Field Name="ChangeFlagAPI" Value="98" />

 </Record>

 <Record>

 <Field Name="NumPedido" Value="888888" />

 <Field Name="ObsCurta" Value="ijlmopq" />

 <Field Name="Status" Value="7" />

 <Field Name="ObjSedex" Value="a8b8c8d8e8" />

 <Field Name="ChangeFlagAPI" Value="99" />

 </Record>

</Records>
```
