# Tratamento de Erros

Diferente do Java ou Python, Go não possui blocos `try/catch`. O tratamento de erros é feito através de valores de retorno explícitos.

!!! tip "Boas Práticas"
    Sempre verifique se o erro é diferente de nulo (`err != nil`) imediatamente após chamar uma função que pode falhar.

## Pacotes de Erro Comuns
| Pacote | Função útil | O que faz |
| :--- | :--- | :--- |
| `errors` | `errors.New()` | Cria um erro simples com uma mensagem de texto. |
| `fmt` | `fmt.Errorf()` | Cria um erro formatado, permitindo injetar variáveis. |

## Exemplo de Código (Retornando Erro)
```go
package main

import (
    "errors"
    "fmt"
)

func dividir(a, b float64) (float64, error) {
    if b == 0 {
        return 0, errors.New("não é possível dividir por zero")
    }
    return a / b, nil
}

func main() {
    resultado, err := dividir(10, 0)
    if err != nil {
        fmt.Println("Erro:", err)
        return
    }
    fmt.Println("Resultado:", resultado)
}