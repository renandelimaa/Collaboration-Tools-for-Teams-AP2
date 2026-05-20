# Introdução e Instalação do Go

O Go (ou Golang) é uma linguagem de programação open source criada pelo Google.

!!! tip "Dica de Instalação"
    Sempre adicione o diretório binário do Go à sua variável de ambiente PATH para rodar os comandos no terminal!

## Tabela de Plataformas Suportadas
| Sistema Operacional | Extensão do Instalador |
| :--- | :--- |
| Windows | `.msi` |
| macOS | `.pkg` |
| Linux | `.tar.gz` |

## Exemplo de Código (Hello World)
```go
package main
import "fmt"

func main() {
    fmt.Println("Olá, Mundo!")
}