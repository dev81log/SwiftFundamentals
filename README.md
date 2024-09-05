# SwiftFundamentals
A comprehensive guide to getting started with the Swift programming language. This resource provides a detailed introduction to the fundamentals of Swift, covering basic syntax, key concepts, and practical examples to help beginners understand and start coding in Swift effectively.


# Guia de Introdução ao Swift

## 1. Introdução ao Swift

Swift é uma linguagem de programação poderosa e intuitiva desenvolvida pela Apple para criar aplicativos para iOS, macOS, watchOS e tvOS. É uma linguagem que combina simplicidade e eficiência, tornando-a ideal tanto para iniciantes quanto para desenvolvedores experientes.

### 1.1 Primeiros Passos: Variáveis e Constantes

No Swift, você pode armazenar valores usando variáveis e constantes. Variáveis são definidas com a palavra-chave `var` e podem ter seus valores alterados ao longo do programa. Constantes são definidas com a palavra-chave `let` e não podem ser alteradas após a sua definição.

```swift
var myVariable = 42
myVariable = 50
let myConstant = 42
```

## 2. Tipos de Dados em Swift

Swift é uma linguagem fortemente tipada, o que significa que cada variável ou constante deve ter um tipo de dado específico, como `Int` para inteiros, `Double` para números decimais, `Bool` para valores booleanos, e `String` para textos.

### 2.1 Exemplos de Tipos de Dados

```swift
let name: String = "Lucas"
let age: Int = 25
let weight: Double = 1.70
let isStudent: Bool = true
```

### 2.2 Desafio: Convertendo Tipos de Dados

#### Desafio 1:
Crie um programa para converter uma `String` no formato `"true"` para um valor Boolean (`Bool`).

```swift
let booleanString = "true"
let booleanConverted = Bool(booleanString)
print(booleanConverted) // Output: true
```

#### Desafio 2:
Converta um número decimal (`Double`) em um número inteiro (`Int`).

```swift
let decimalNumber: Double = 20.1
let integerNumber: Int = Int(decimalNumber)
print(integerNumber) // Output: 20
```

## 3. Operadores em Swift

Operadores são usados para realizar operações em variáveis e constantes. Swift oferece uma variedade de operadores, incluindo aritméticos, de comparação e lógicos.

### 3.1 Operadores Aritméticos e Lógicos

```swift
var x = 10
x += 1  // x agora é 11
x -= 1  // x agora é 10
x *= 2  // x agora é 20
x /= 2  // x agora é 10

let y = 10
let isEqual = y == 10  // true
let isGreaterThan = y > 5  // true
let isTrue = true
let isFalse = false

isTrue && isFalse  // false
isTrue || isFalse  // true
!isTrue  // false
```

### 3.2 Desafio: Trabalhando com Operadores Lógicos

1. Compare a igualdade de duas `Strings`.
2. Verifique se uma pessoa pode dirigir com base em sua idade.
3. Inverta a lógica para verificar se a pessoa NÃO pode dirigir.
4. Verifique se a pessoa é motorista OU tem 17 anos ou mais.
5. Verifique se a pessoa é motorista E tem mais de 30 anos.

```swift
let stringA = "Lucas"
let stringB = "Lucas"
let isEqual = stringA == stringB
print(isEqual) // true

let age = 18
let canDrive = age >= 18
print(canDrive) // true

let cannotDrive = age < 18
print(cannotDrive) // false

let isDriver = true
let isAdult = age >= 17
let canDriveOrIsAdult = isDriver || isAdult
print(canDriveOrIsAdult) // true

let isOlderDriver = isDriver && age > 30
print(isOlderDriver) // false
```

## 4. Controle de Fluxo

Swift permite que você controle o fluxo de execução do seu programa usando condicionais e loops.

### 4.1 Condicionais: `if`, `else`, `switch`

```swift
let temperature = 30

if temperature > 25 {
    print("Está quente lá fora!")
} else {
    print("Está frio lá fora!")
}

let dayOfWeek = "Segunda"

switch dayOfWeek {
case "Segunda":
    print("Início da semana.")
case "Sexta":
    print("Fim da semana.")
default:
    print("Outro dia da semana.")
}
```

### 4.2 Loops: `for`, `while`

```swift
for i in 1...5 {
    print(i)
}

var counter = 5
while counter > 0 {
    print(counter)
    counter -= 1
}
```

### 4.3 Desafio: Aplicando Controle de Fluxo

Crie um loop que conte de 1 a 10 e, para cada número, verifique se é par ou ímpar.

```swift
for i in 1...10 {
    if i % 2 == 0 {
        print("\(i) é par")
    } else {
        print("\(i) é ímpar")
    }
}
```

## 5. Funções e Escopo

Funções são blocos de código que executam tarefas específicas. No Swift, você pode declarar e usar funções para organizar e reutilizar seu código.

### 5.1 Declaração e Uso de Funções

```swift
func greet(name: String) -> String {
    return "Olá, \(name)!"
}

let greeting = greet(name: "Lucas")
print(greeting) // Output: Olá, Lucas!
```

### 5.2 Escopo de Variáveis

Variáveis declaradas dentro de uma função são locais e não podem ser acessadas fora dela.

```swift
func calculateSum(a: Int, b: Int) -> Int {
    let sum = a + b
    return sum
}

let result = calculateSum(a: 5, b: 10)
print(result) // Output: 15
```

### 5.3 Desafio: Criando Funções Personalizadas

Crie uma função que receba um número como parâmetro e retorne se ele é par ou ímpar.

```swift
func isEven(number: Int) -> Bool {
    return number % 2 == 0
}

let number = 4
let result = isEven(number: number)
print(result) // Output: true
```

## 6. Coleções em Swift

Swift oferece três tipos principais de coleções: Arrays, Dicionários e Conjuntos.

### 6.1 Arrays

```swift
var fruits = ["Apple", "Banana", "Orange"]
fruits.append("Mango")
print(fruits) // Output: ["Apple", "Banana", "Orange", "Mango"]
```

### 6.2 Dicionários

```swift
var carPrices = ["Toyota": 20000, "BMW": 35000, "Audi": 40000]
carPrices["Mercedes"] = 45000
print(carPrices) // Output: ["Toyota": 20000, "BMW": 35000, "Audi": 40000, "Mercedes": 45000]
```

### 6.3 Conjuntos

```swift
var uniqueNumbers: Set = [1, 2, 3, 4, 5]
uniqueNumbers.insert(6)
print(uniqueNumbers) // Output: [1, 2, 3, 4, 5, 6]
```

### 6.4 Desafio: Manipulação de Coleções

1. Crie um array de números inteiros e some todos os elementos.
2. Crie um dicionário para armazenar nomes e idades, e então encontre a idade de um nome específico.

```swift
let numbers = [1, 2, 3, 4, 5]
let sum = numbers.reduce(0, +)
print(sum) // Output: 15

let people = ["Lucas": 25, "Mariana": 30, "Pedro": 22]
if let age = people["Mariana"] {
    print(age) // Output: 30
}
```

## 8. Optionals

Os optionals em Swift são usados para representar valores que podem estar ausentes. Um optional é uma variável que pode conter um valor ou `nil`.

### 8.1 Declaração de Optionals

```swift
var optionalString: String? = "Hello"
```

### 8.2 Desembrulhando Optionals

Para acessar o valor de um optional, você pode "desembrulhá-lo" usando `if let` ou `guard let`.

```swift
if let unwrappedString = optionalString {
    print(unwrappedString) // Output: Hello
} else {
    print("optionalString is nil")
}
```

Outra maneira é usar o operador `!`, mas isso deve ser feito com cuidado, pois pode causar erros se o optional estiver `nil`.

```swift
print(optionalString!) // Force Unwrapping (Use com Cuidado)
```

## 9. Classes e Herança

Swift também suporta programação orientada a objetos com classes. As classes, ao contrário das structs, suportam herança.

### 9.1 Declaração de Classes

```swift
class Animal {
    var name: String

    init(name: String) {
        self.name = name
    }

    func makeSound() -> String {
        return "Some sound"
    }
}

let dog = Animal(name: "Dog")
print(dog.name) // Output: Dog
```

### 9.2 Herança

Uma classe pode herdar propriedades e métodos de outra classe.

```swift
class Dog: Animal {
    override func makeSound() -> String {
        return "Woof"
    }
}

let dog = Dog(name: "Dog")
print(dog.makeSound()) // Output: Woof
```

## 10. Protocolos

Os protocolos em Swift definem um "contrato" ou conjunto de métodos e propriedades que uma classe ou struct deve implementar.

### 10.1 Declaração de Protocolos

```swift
protocol Greetable {
    func greet() -> String
}

class Person: Greetable {
    var name: String

    init(name: String) {
        self.name = name
    }

    func greet() -> String {
        return "Hello, \(name)"
    }
}

let person = Person(name: "Lucas")
print(person.greet()) // Output: Hello, Lucas
```

## 11. Enumerations (Enums)

Enums em Swift são tipos que permitem trabalhar com valores definidos em um conjunto fechado.

### 11.1 Declaração de Enums

```swift
enum Direction {
    case north
    case south
    case east
    case west
}

var direction = Direction.north
direction = .east
```

### 11.2 Enums com Valores Associados

Enums também podem armazenar valores associados.

```swift
enum Barcode {
    case upc(Int, Int, Int, Int)
    case qrCode(String)
}

var productBarcode = Barcode.upc(8, 85909, 51226, 3)
productBarcode = .qrCode("ABCDEFGHIJKLMNOP")
```

## 12. Extensions

Extensions permitem adicionar novas funcionalidades a um tipo existente, como uma struct, uma classe ou um tipo primitivo, sem a necessidade de modificar o código original.

### 12.1 Criando uma Extension

```swift
extension String {
    func reversed() -> String {
        return String(self.reversed())
    }
}

let greeting = "Hello"
print(greeting.reversed()) // Output: "olleH"
```

## 13. Conclusão

Neste guia, abordamos os conceitos básicos e avançados do Swift, incluindo variáveis, constantes, tipos de dados, operadores, controle de fluxo, funções, coleções, structs, optionals, classes, herança, protocolos, enums e extensions. Com esse conhecimento, você está bem equipado para continuar explorando Swift e desenvolver aplicativos robustos para a plataforma Apple.

### Próximos Passos no Estudo de Swift

- Explore frameworks do iOS como UIKit e SwiftUI.
- Aprenda sobre programação orientada a objetos em Swift.
- Crie projetos práticos para consolidar seu aprendizado.



