# Arrays, Slices e Maps

Em Go, usamos Arrays (tamanho fixo), Slices (tamanho dinâmico) e Maps (chave-valor) para armazenar coleções de dados.

!!! warning "Cuidado com Arrays"
    Arrays em Go têm tamanho fixo. Se você precisar de uma lista que cresce, use Slices!

## Comparação de Estruturas
| Estrutura | Tamanho | Como inicializar |
| :--- | :--- | :--- |
| **Array** | Fixo | `var a [5]int` |
| **Slice** | Dinâmico | `s := make([]int, 0)` |
| **Map** | Dinâmico | `m := make(map[string]int)` |

## Exemplo de Código (Slice e Map)
```go
package main
import "fmt"

func main() {
    // Slice
    frutas := []string{"Maçã", "Banana"}
    frutas = append(frutas, "Laranja")

    // Map
    idades := map[string]int{
        "Cauã": 20,
        "Renan": 21,
    }
    fmt.Println(frutas, idades)
}