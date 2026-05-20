# Testes em Go

A linguagem Go já vem com um framework de testes embutido, sem necessidade de instalar bibliotecas externas.

!!! note "Regra de Ouro dos Nomes"
    Os arquivos de teste devem obrigatoriamente terminar com `_test.go` e as funções começar com `Test` (T maiúsculo).

## Comandos de Teste
| Comando | O que faz |
| :--- | :--- |
| `go test` | Roda todos os testes do pacote atual |
| `go test -v` | Roda com modo verboso (mostra detalhes) |
| `go test -cover` | Mostra a porcentagem de cobertura do código |

## Exemplo de Código (soma_test.go)
```go
package main
import "testing"

func Soma(a, b int) int {
    return a + b
}

func TestSoma(t *testing.T) {
    resultado := Soma(2, 3)
    esperado := 5
    
    if resultado != esperado {
        t.Errorf("Erro: esperava %d, mas recebeu %d", esperado, resultado)
    }
}