# golang-homework

# Домашнее задание к занятию "7.5. Основы golang"

## Задача 1. Установите golang.

    c:\Oleg>go version
    go version go1.17.2 windows/amd64


    c:\Oleg\GO>go run test.go
    Hello, World!

    c:\Oleg\GO>

## Задача 2. Знакомство с gotour. - done

## Задача 3. Написание кода.

### 	3.1 Напишите программу для перевода метров в футы

    package main

    import "fmt"

    func main() {
        fmt.Print("введите в метрах: ")
        var input float64
        fmt.Scanf("%f", &input)

        output := input / 0.3048

        fmt.Println("в футах будет  ", output)
    }


### 	3.2 Напишите программу, которая найдет наименьший элемент в любом заданном списке, например:
x := []int{48,96,86,68,57,82,63,70,37,34,83,27,19,97,9,17,}


    package main

    import "fmt"

    func main() {

        x := []int{48, 96, 86, 68, 57, 82, 63, 70, 37, 34, 83, 27, 19, 97, 9, 17}

        mini := x[0]

        length := len(x)

            for i := 0; i<length; i = i+1 {

                  if x[i] < mini {
                  mini = x[i]
                  }
            }
        fmt.Println(mini)
    }


### 	3.3 Напишите программу, которая выводит числа от 1 до 100, которые делятся на 3. То есть (3, 6, 9, …)

    package main

    import "fmt"

    func main() {

            for i := 1; i<101; i = i+1 {
                  if i % 3 == 0  {
                  fmt.Println(i)
                  }
            }
    }


Задача 4. Протестировать код (не обязательно).

Для задачи 3.2

    package main
    import "testing"

    func testMain(t *testing.T) {

        v := mini
        if v != 9 {
         t.Error("Expected 9, got ", v)
         }

       }




