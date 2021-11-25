
# Uruchamianie programu `go` w VS Code

`go get -v golang.org/x/tools/cmd/goimports`

`go run .\test1.go`

---

```go
package main

import (
	"fmt"
	"math"
)

func main() {
	//fmt.Println(math.pi) //pi is unexported
	fmt.Println(math.Pi)
}
```

---

```go
package main

import "fmt"

func add(x int, y int) int {
	return x + y
}

func main() {
	fmt.Println(add(42, 13))
}
```

---

```go
package main

import "fmt"

func add(x int, y int) int {
	return x + y
}

func doubleAndAdd(x int, y int) int {
	var xx int
	xx = 2*x
	var yy int
	yy = 2*y
	return xx+yy
}

func main() {
	fmt.Println(add(42, 13))
	fmt.Println(doubleAndAdd(2, 3))
}
```

---

# Standardowa deklaracja: 

```go
x int, y int
func foo(x int, y int) {

Skrócona deklaracja:

x, y int
func foo(x, y int) {
```

---

```go
package main

import "fmt"

func add(x, y int) int {
	var xx, yy int
	xx = x
	yy = y
	return xx + yy
}

func main() {
	fmt.Println(add(42, 13))
}
```

---

# Deklaracja i osobne przypisanie

```go
var x int
x = 10

deklaracja z przypisaniem

x := 10
```

---

# Zwracanie kilku wartości z funkcji

```go
package main

import "fmt"

func swap(x, y string) (string, string, int) { 
	var xx int
	xx = 10
	
	yy := 10
	return y, x, xx+yy
}

func main() {
	a, b, _ := swap("hello", "world") //ostatnie nie wykorzystana 
	fmt.Println(a, b)
}
```

--- 

# Nazwane wartości zwracane (_naked return_)

```go
package main

import "fmt"

func split(sum int) (x, y int) {
	x = sum * 4 / 9
	y = sum - x
	return
}

func get25and75perc(value float32) (res25, res75 float32) { //nazwane zmienne
	res25 = value * 0.25
	res75 = value * 0.75
	return //wystarczy: zwrócone zostaną nazwane zmienne
}
```
func main() {
	fmt.Println(split(17))
	fmt.Println(get25and75perc(100))
}

---

# Łańcuchowa deklaracja zmiennych

```go
package main

import "fmt"

//package level declaration
var c, python, java bool

var isC, isPython, isJava bool 		//list declaration of boolean variables
var age, salary, length float32 	//list declaration of float variables

//function level declaration
func main() {
	var name, surname string 		//list declaration of string variables
	var i int
	fmt.Println(i, c, python, java)
	fmt.Println(isC, isPython, isJava, age, salary, length, name, surname)
}
```

---

# Deklaracja wraz z inicjalizacją

```go
package main

import "fmt"

//deklaracja i inicjalizacja z podaniem typu
var i, j int = 1, 2

//deklaracja z inicjalizacją bez podania typu
var a, b, c = false, 0.123, "yes"

func main() {
	var c, python, java = true, false, "no!"
	fmt.Println(i, j, c, python, java)
}
```

---

# Skrócona deklaracja z inicjalizacją

```go
package main

import "fmt"

func main() {
	var i, j int = 1, 2
	k := 3
	c, python, java := true, false, "no!"

	fmt.Println(i, j, k, c, python, java)
}
```

# Podstawowe typy

```go
package main

import (
	"fmt"
)

func main() {

	var x = 2.0
	var y float64 = 2
	var p1 rune = 32
    var c1 complex128 = complex128(4 + 2i)

	fmt.Print(x + y + 1.2 + float64(p1) + real(c1) + imag(c1))
}

//inne typy:
//int int8 int16 int32 int64
//uint uint8 unit16 unit32 unit64
//unitptr //uint pointer
//byte (alias for uint8)
//rune (alias for int32) //zwraca podany kod w postaci znaku ni
//float32, float64
//complex64, complex128

```

---

# Konwersja typów

```go
var x int = 2
var y uint = uint(x)
```

```go
x := 2
y := uint(x)
```

---

# Wyświetlanie typów i typ dowolny

```go
package main

import "fmt"

func printType(value interface{}) {
	fmt.Printf("%T\n", value)
}

func main() {

	i := 2                  //int
	f := 2.0                //float64
	s := "abc"              //string
	b := true               //bool
	c := complex128(1 + 2i) //complex128

	printType(i)
	printType(f)
	printType(s)
	printType(b)
	printType(c)
}

//go run .\test1.go
```

---

# Stałe

```go
package main

import "fmt"

const pi = 3.14
const abc = "abc"
const yes = true

func main() {

	fmt.Println(pi)
	fmt.Println(abc)
	fmt.Println(yes)
}

//go run .\test1.go
```

---

# Pętla `for`

```go
package main

import (
	"fmt"
)

func main() {

	//for loop
	for i := 0; i < 10; i++ {
		fmt.Println(i)
	}

	//while loop
	i := 0
	for i < 10 {
		fmt.Println(i)
		i += 1
	}

}

//go run .\test1.go

```

# Wyrażenie `if`

```go
package main

import (
	"fmt"
)

func main() {

	for i := 0; i < 10; i++ {

		//if
		if i%2 == 0 {
			fmt.Println("If i%2 == 0\ti = %i", i)
		}

		//if with variable
		if j := 2 * i; j%3 == 0 {
			fmt.Println("\tIf j%3 == 0\tj = %i", j)
		}

	}

}

//go run .\test1.go
```

# Przykład: numeryczne wyznaczenie liczby

Zadanie: dla danego $x$ znaleźć takie $z$, że $z^2 \approx x$.

Wzór na kolejne przybliżenia: 

$$
z = z - \frac{z^2 - x}{2z}
$$

```go
package main

import (
	"fmt"
)

func FindNextApprox(prev float64, goal float64) (next float64) {

	fmt.Printf("Prev: %f\tprev^2: %f\tprev^2-goal: %f\n", prev, prev*prev, prev*prev-goal)

	next = (prev*prev - goal) / (2 * prev)
	return
}

func main() {

	x := 4.0
	z := 1.0

	for i := 0; i < 10; i++ {

		z -= FindNextApprox(z, x)

		fmt.Println(z)
	}

}

//go run .\test1.go

```

# Switch

```go
package main

import (
	"fmt"
	"runtime"
)

func main() {

	os := runtime.GOOS

	switch val := os; val {
	case "windows":
		fmt.Println("It's Windows")
	case "linux":
		fmt.Println("It's Linux")
	default:
		fmt.Println("I don't know...")
	}

}

//go run .\test1.go
```

# Pattern matching

```go
package main

import (
	"fmt"
)

func main() {

	input := "c"

	switch {
	case input == "a":
		fmt.Println("It's 'a'")
	case input == "b":
		fmt.Println("It's 'b'")
	case input == "c":
		fmt.Println("It's 'c'")
	default:
		fmt.Println("I don't know")

	}
}

//go run .\test1.go
```

# `defer`

```go
package main

import (
	"fmt"
)

func foo1() { fmt.Println("Do this first") }
func foo2() { fmt.Println("Do this next") }
func foo3() { fmt.Println("Do this last") }

func main() {

	defer foo1()

	defer foo2()

	foo3()
}

//Do this last
//Do this next
//Do this first

//go run .\test1.go
```











