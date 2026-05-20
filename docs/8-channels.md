# Channels (Canais)

Channels são os canos que conectam as *goroutines*. Eles permitem que diferentes threads do Go conversem e enviem dados entre si de forma segura.

!!! danger "Deadlock!"
    Se uma goroutine tentar ler de um canal vazio e ninguém enviar nada, o programa vai travar num erro fatal chamado Deadlock.

## Tipos de Canais
| Tipo | Comportamento | Exemplo de Criação |
| :--- | :--- | :--- |
| **Unbuffered** | Bloqueia até o receptor estar pronto | `make(chan int)` |
| **Buffered** | Aceita N valores antes de bloquear | `make(chan int, 5)` |

## Exemplo de Código (Enviando e Recebendo)
```go
package main
import "fmt"

func enviarMensagem(canal chan string) {
    canal <- "Olá do Canal!" // Envia o dado
}

func main() {
    meuCanal := make(chan string)
    go enviarMensagem(meuCanal)
    
    mensagem := <-meuCanal // Recebe o dado
    fmt.Println(mensagem)
}