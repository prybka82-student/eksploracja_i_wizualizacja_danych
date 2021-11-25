Projektowanie rozwiązań internetowych - lab. - dr Łukasz Więcław - 19.02.2021

PRI_lab_2021-02-19

kod do zesp. w Teamsach
ad72ehl

# golang

Szybki i wygodny język do tworzenia backendów. 

Nie w pełni obiektowy: logika biznesowa powinna być prosta, a klasy zawsze są zasobożerne. 

Np. hello world w c++ - ok. 300KB, c - ok. 100KB, c## - kilkaset MB ze względu na dołączenie całego środowiska uruchomieniowego.

!!!Przerobić tutorial:

https://tour.golang.org/welcome/1

!!!Poszukać środowiska programistycznego

!!!Zrobić pierwsze dowolne zadanie z: 
https://gophercises.com/

---

package main

import (
	"fmt"
	//"time"
	"math/rand"
)

func main() {
	//rand.Seed(time.Now().UnixNano())
	rand.Seed(9)
	fmt.Println("My favorite number is", rand.Intn(10))
}

---

# Zaliczenie

Projekt - każdy oddzielnie, własna aplikacja z backended w Go i Kubernetes, frontend w dowolnej technologii.

---

# GO w VS Code

https://code.visualstudio.com/docs/languages/go

---

# IDE

https://www.tabnine.com/blog/top-7-golang-ides-for-go-developers/

---

package main

import (
	"fmt"
	"math"
)

func main() {
	//fmt.Println(math.pi) //pi is unexported
	fmt.Println(math.Pi)
}


---

package main

import "fmt"

func add(x int, y int) int {
	return x + y
}

func main() {
	fmt.Println(add(42, 13))
}

---

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

---

Standardowa deklaracja: 

x int, y int
func foo(x int, y int) {

Skrócona deklaracja:

x, y int
func foo(x, y int) {

---

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

---

deklaracja i osobne przypisanie

var x int
x = 10

deklaracja z przypisaniem

x := 10

---

Zwracanie kilku wartości z funkcji

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

--- 

Nazwane wartości zwracane

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

func main() {
	fmt.Println(split(17))
	fmt.Println(get25and75perc(100))
}

---

Łańcuchowa deklaracja zmiennych

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

---

Deklaracja wraz z inicjalizacją

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

---

Skrócona deklaracja z inicjalizacją

package main

import "fmt"

func main() {
	var i, j int = 1, 2
	k := 3
	c, python, java := true, false, "no!"

	fmt.Println(i, j, k, c, python, java)
}







































