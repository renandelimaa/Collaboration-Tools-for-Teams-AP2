# Sintaxe e Variáveis

A sintaxe de Go é limpa e concisa. A linguagem possui forte tipagem estática.

!!! info "Declaração Curta"
    Dentro de funções, você pode usar `:=` para declarar e inicializar uma variável na mesma linha, sem precisar digitar `var`.

## Tipos Básicos Primitivos
| Tipo | Descrição | Exemplo de Uso |
| :--- | :--- | :--- |
| `int`, `float64` | Números inteiros e decimais | `idade := 25` |
| `string` | Textos | `nome := "Renan"` |
| `bool` | Verdadeiro ou Falso | `ativo := true` |

## Exemplo de Código
```go
package main
import "fmt"

func main() {
    var linguagem string = "Go"
    versao := 1.21 // Tipagem inferida
    
    fmt.Printf("Estudando %s na versão %.2f\n", linguagem, versao)
}