# Concorrência com Goroutines

Uma goroutine é uma função que executa de forma concorrente com outras funções na mesma aplicação.

!!! danger "Perigo de Execução"
    Se a função `main` terminar, todas as goroutines em andamento são encerradas imediatamente! Use `sync.WaitGroup` para evitar isso.

## Comparativo: Goroutines vs Threads
| Característica | Goroutine | Thread do SO |
| :--- | :--- | :--- |
| Memória inicial | ~2 KB | ~1 a 2 MB |
| Gerenciamento | Pelo Go Runtime | Pelo Sistema Operacional |

## Exemplo de Código (Iniciando uma Goroutine)
```go
package main
import (
    "fmt"
    "time"
)

func ola() {
    fmt.Println("Olá da Goroutine!")
}

func main() {
    go ola() // O "go" inicia a concorrência
    time.Sleep(1 * time.Second)
}
