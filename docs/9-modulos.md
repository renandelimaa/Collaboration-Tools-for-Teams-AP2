# Gerenciamento com Go Modules

O Go Modules é o sistema oficial de gerenciamento de dependências da linguagem.

!!! tip "Arquivo go.sum"
    Nunca apague o arquivo `go.sum` manualmente! Ele contém os hashes de segurança (checksums) das bibliotecas que você baixou.

## Comandos Principais
| Comando | O que faz |
| :--- | :--- |
| `go mod init [nome]` | Inicializa um novo módulo no projeto |
| `go mod tidy` | Remove dependências não usadas e baixa as que faltam |
| `go get [pacote]` | Baixa um pacote específico |

## Exemplo de Código (Usando um pacote externo)
```go
package main

import (
    "fmt"
    "[github.com/google/uuid](https://github.com/google/uuid)" // Exemplo de pacote baixado
)

func main() {
    id := uuid.New()
    fmt.Println("ID gerado:", id)
}
