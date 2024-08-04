# APP Reactive

# Cliclo de Vida de um Screen

 - tanto no Out mobile como o reactive web App seguem um ciclo de vida especifico

 - Dados da tela -> para. de entrada, Variaveis e agregados acoes de dados

    initialize -> Ready -> Render -----------------|    Render
  
        entrada de novos dados -> Fetch ------------|


        entre telas ocorre uma sequencia parecida

        repete os passos e durante o transição destroi a tela antiga

        mudança de parametros
          chance parameters -> Render(block) -> render screen
  
  - Eventos relacionados ao ciclo de vida:
    
    - On initialize
    - On ready
    - On Render
    - On After Fetch
    - On parameters Changed
    - On Destroy