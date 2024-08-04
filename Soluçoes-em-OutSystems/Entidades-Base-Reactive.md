# Entidades 

 - entidades são tabelas que representa um conjunto de dados no banco
 - uma entidade e definida por seus atributos
   - por exemplo em um tabela clientes os atributos da entidade seriam 
      - Nome, endereço, plano_assinado, telefone, etc

- criar novo atb a uma tabela existente
- em caso de remoção tem que tomar cuidado, pois o dado pode estar sendo usado por outra tabela, ou ser dependente de outro
  geralmente isso inclue opçoes de delete como O cascate e similares não sei aqui no OUT


# Relacionamento de Entidades

 - o relacionamento de entidades e definido pela famosa "foreign key" 
    - a chave estrangeira tem o intuito de se referir a uma segunda tabela
    - no Out ele e do tipo Entity Identifier
    - As relaçoes podem ser:
      - Um a UM
       o id de uma tabela Funcionario, que tem um entidade  foto, faz referencia a outra tabela que contem a fota( a chave estrangeira seria ContactId)
       - ou seja cada contato tem apenas um contact Id
      - um para muitos
        - por exemplo uma entidade empresa tem uma tabela Funcionarios, e que cada individo dessa tabela faz referencia a outras tabelas com as informaçoes dos funcionario
      - muitos para muitos
        Uma empresa tem muitos contatos mas o mesmo contato tambem tem contato com outras empresas
        - geralmento e uma tabela intermediaria entre elas

# Regras de Exclusão

  - No OUT tem 3 tipos de regras:
    - Protect -> Se existir o id do dado a ser deletado em outra tabela, o Out barra a exclusão
    - Delete -> nesse caso ira deletar o dado e todas as suas referencias
    - Ignore -> Não a validação na hora de remover( não ententi a explicação do cara muito)

# tabelas Estaticas e normais
 
  - a estatica ja vem com 4 atb( id, label, order e isActive )
  - a estatica tem que ser adicionada na pasta records, devido a sua natureza
    - tem que se adicionar a mão
    - vc cria no recordes as row que irão ser adicionadas pelo que entendi
     - cada uma vira com os atb default, id(auto increment), Label( o nome escolhido), Order e Isactive

  - Na tabela normal não vem atb pre-definidos e vc cria as colunas
  - o Id da tabela é automatico
  - da para fazer modelos de tabelas no diagrama

# Obtenção de Dados

 - obter os dados do banco para mostra-lo na tela
 - no Out tem duas formas, data action e os agregates

 - Agregate e criado na hora de colocar criar uma entidade para mostrar na tela
    - arrastando uma entidade previamente criada ela ira aparecer na tela
    - se essa tabela tiver alguma ligação com outro , essa sera automaticamente arrastada
    - Ira ser criado um area de join( SQL) e voce pode pesquisar de 3 maneiras:
      - only with: ira exibir somente os elementos da tabela 1 que tenham conexão com tabela2
      - with or without: com o sem ligação
      - without: somente os elementos sem ligação alguma com a tabela 2

    - Isso automaticamente ira gerar criar na area de interface um getItem que pode ser arrastado para a tela de interface para visualizar a tabela

    - acesso tem o registrado( so pessoas registradas e anomimos, qualquer pessoa)