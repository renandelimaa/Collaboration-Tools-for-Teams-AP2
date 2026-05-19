# Estruturas de Controle em Go

Em Go, não temos o laço `while` ou `do-while`. O único laço de repetição é o `for`.

!!! warning "Atenção com as chaves"
    No Go, a chave de abertura `{` deve ficar obrigatoriamente na mesma linha do comando `if` ou `for`.

## Tabela de Operadores Relacionais
| Operador | Significado | Exemplo |
| :--- | :--- | :--- |
| `==` | Igual a | `a == b` |
| `!=` | Diferente de | `a != b` |
| `<=` | Menor ou igual | `a <= b` |

## Exemplo de Código (Laço For)
```go
package main
import "fmt"

func main() {
    for i := 0; i < 5; i++ {
        fmt.Println("Contador:", i)
    }
}