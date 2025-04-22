# Aprendendo Golang - Guia Básico para Iniciantes 🐹

Este é um guia simples e direto para quem quer começar a programar com **Golang (Go)**. Aqui você vai aprender os conceitos básicos que precisa para entender como a linguagem funciona e como escrever seus primeiros códigos.

---

## 📦 Estrutura básica de um programa Go

```go
package main

import "fmt"

func main() {
    fmt.Println("Olá, mundo!")
}
```

- `package main`: Todo programa Go começa com um pacote. O pacote `main` indica que é o ponto de entrada da aplicação.
- `import "fmt"`: Usado para importar pacotes (como bibliotecas). O `fmt` permite imprimir no terminal.
- `func main() {}`: A função principal, onde o programa começa a rodar.

---

## 📚 Imports

Para usar funcionalidades extras, você importa pacotes:

```go
import (
    "fmt"
    "math"
)
```

- Use `()` para importar vários pacotes de uma vez.
- Ex: `math.Sqrt(4)` retorna a raiz quadrada de 4.

---

## 🔧 Funções

```go
func saudacao(nome string) string {
    return "Olá, " + nome
}

func main() {
    mensagem := saudacao("Maria")
    fmt.Println(mensagem)
}
```

- `func`: Define uma função.
- `(nome string)`: Parâmetro com tipo.
- `string`: Tipo do valor de retorno.

---

## 🔁 Laço de repetição (for)

```go
func main() {
    for i := 0; i < 5; i++ {
        fmt.Println("Número:", i)
    }
}
```

- `for` é o único laço de repetição do Go.
- Pode ser usado como `while` também:

```go
i := 0
for i < 5 {
    fmt.Println(i)
    i++
}
```

---

## 🙈 if / else

```go
idade := 18

if idade >= 18 {
    fmt.Println("Maior de idade")
} else {
    fmt.Println("Menor de idade")
}
```

---

## 📦 Variáveis

```go
var nome string = "João"
idade := 25 // Inferência de tipo

fmt.Println(nome, idade)
```

- `var` define variáveis com tipo explícito.
- `:=` cria variáveis com tipo inferido automaticamente.

---

## 🧮 Tipos de dados

- `string`: Texto
- `int`, `int64`: Números inteiros
- `float64`: Números com vírgula
- `bool`: verdadeiro/falso

---

## 📦 Arrays e Slices

```go
// Array
var numeros [3]int = [3]int{1, 2, 3}

// Slice (mais usado)
nomes := []string{"Ana", "Bruno", "Carlos"}

fmt.Println(nomes[0]) // Ana
```

---

## 🔁 Range

```go
for i, nome := range nomes {
    fmt.Println(i, nome)
}
```

- `range` percorre arrays, slices, maps e strings.

---

## 🧹 defer

```go
func main() {
    defer fmt.Println("Fim")
    fmt.Println("Início")
}
```

- `defer` adia a execução de algo até o final da função.
- Muito útil para fechar arquivos, conexões, etc.

---

## 🗂 Estruturas (structs)

```go
type Pessoa struct {
    Nome string
    Idade int
}

func main() {
    p := Pessoa{Nome: "Lucas", Idade: 30}
    fmt.Println(p.Nome)
}
```

---

## 🔄 Funções com múltiplos retornos

```go
func dividir(a, b int) (int, int) {
    return a / b, a % b
}

func main() {
    resultado, resto := dividir(10, 3)
    fmt.Println("Resultado:", resultado, "Resto:", resto)
}
```

---

## 🐛 Erros

```go
import "errors"

func fazerAlgo() error {
    return errors.New("algo deu errado")
}
```

---

## 🧪 Comandos úteis

- `go run arquivo.go` – roda seu código.
- `go build` – compila o projeto.
- `go mod init nome-do-projeto` – inicia um módulo Go.
- `go get` – instala bibliotecas externas.
- `go fmt` – formata seu código.
- `go test` – roda testes.

---

## 📘 Dica final

A documentação oficial do Go é excelente e vale a pena visitar:  
📎 https://golang.org/doc/

---

Boa sorte na jornada com Golang! 🚀
