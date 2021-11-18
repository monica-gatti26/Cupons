# language: pt
@browser
Funcionalidade: Cupom de desconto

 
Esquema do Cenario: Validar cupons com sucesso
    Dado que eu acesse o site "QASTOREDESAFIO.LOJAINTEGRADA.COM.BR"
    E "<PréCondição>"
    Quando aplicar cupom "<variaçãodecupons>"
    Então será aprentado o comportamento "<ComportamentoEsperado>"

    Exemplos: 
      |PréCondição:                            | variaçãodecupons:                        | ComportamentoEsperado:                                                 |
      |Não tiver utilizado o cupom             |CupomFreteGratis                          |Desconto do frete com sucesso                                           |
      |Não tiver utilizado o cupom             |CupomItensCarrinho                        |Desconto em apenas itens do carrinho difrenciando dos itens sem desconto|
      |Já tiver usado cupom de frete gratis    |CupomFreteGratis                          |Cupom já utilizado                                                      |
      |Tiver desconto no pagamento á vista     |30REAIS                                   |Desconto será mantido no pagamento a vista e cupom de desconto aplicado |
      |Efetuar uma compra de 299,99            |Cupom de 30 para compras Apartir 300REAIS |mensagem que a compra não atingiu o valor para utilização do cupom      |
      |Efetuar uma compra de 300,00            |Cupom de 30 para compras Apartir 300REAIS |Cupom aplicado com Sucesso                                              |
      |Efetuar uma acima de 300,00             |Cupom de 30 para compras Apartir 300REAIS |Cupom aplicado com Sucesso                                              |
      |Já tiver usado cupom 30OFF              |Cupom30OFF                                |Cupom já utilizado                                                      |
      |Usar Cupom vencido                      |Cupom10OFF                                |Cupom expirado                                                          | 
      |Inserir Cupom com informações incorreta |CupomErrad@                               |Cupom incorreto ou expirado                                             | 


















