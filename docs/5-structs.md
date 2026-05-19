# Structs e Métodos

O Go não possui "Classes" como o Java. Em vez disso, usamos `structs` para agrupar dados.

!!! note "Herança em Go?"
    Go não suporta herança tradicional, mas você pode usar a "Composição" embutindo structs umas nas outras!

## Tipos de Métodos (Receivers)
| Tipo de Receiver | Modifica a Struct original? | Recomendação de uso |
| :--- | :--- | :--- |
| Valor (`T`) | Não (faz uma cópia) | Structs pequenas |
| Ponteiro (`*T`) | Sim | Quando precisa alterar o dado |

## Exemplo de Código (Struct e Método)
```go
package main
import "fmt"

type Pessoa struct {
    Nome string
    Idade int
}

func (p Pessoa) Apresentar() {
    fmt.Println("Olá, meu nome é", p.Nome)
}