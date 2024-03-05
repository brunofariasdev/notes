
**O EntityFramework Core e uma versão mais leve do EntityFramework, ele permite trabalhar com o banco de dados usando objetos  .NET .**

------

## Criando Um Projeto

`dotnet new console -o FirstProjectEntityCore` 

## Instalação

`dotnet add package -o Microsoft.EntityFrameworkCore.SqlServer`

# Operação dos Dados

- Os Dados podem ser excluídos,  editados e criados usando suas classes de entidades.

## Projeto de  uma biblioteca pessoal

- Temos aqui a primeira entidade um Book esse book e uma entidade filha e vai precisar conter uma referencia um método de acesso a sua entidade mãe a Library

```c# 
public class Book{
    public int Id {get; set;}
    public string Name {get; set;} 
    public string gender {get; set;}
    //Referencia da chave extrangeira da Library
    public int LibraryId {get; set;}
    //Entidade Library
    public virtual Library Library {get; set;}
}
```

- Aqui temos a entidade principal mãe que teremos uma referencia a lista de entidades filhas Book

```c#
public class Library{
    public int Id {get; set;}
    public string Author {get; set;}
    //Nessa entidade iremos acessar nossa lista de Books que fazem parte essa Library
    public virtual Books {get; set;}
}
```

- Cada entidade dessa representa uma tabela do nosso banco de dados logo abaixo vamos configurar nossa chave estrangeira e nossas chaves primarias fazendo criando assim nossa relação entre as tabelas.

## DbContext

- O DbContext e a classe central do EntityFramework e ela quem permite que a gente interaja com o banco de dados usando as entidade, ele basicamente funciona como uma ponte entre o código e o banco de dados.
### Nosso DbContext

