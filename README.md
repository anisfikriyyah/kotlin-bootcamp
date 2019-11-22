# Kotlin Bootcamp

## Operator

1+1

2-1

3.1/1.3

5*2

## Integer

#### Int primitif digunakan sebagai objek

```kotlin
1.toLong()
//1
```

### Letakkan Int dalam variable

```kotlin
val boxed: Number = 1
boxed.toLong()
// 1
```

### Variable

Untuk menyimpan data secara permanen letakkan data tersebut kedalam sebuah variable.
Variable ada 2 tipe, yaitu changeable dan unchangable.

`Val` dan `Var`

```kotlin
val aquarium = 1
// 1

aquarium = 2
// error: val cannot be reasign
```

```kotlin
var day = "Sunday"
// Sunday
day = "Friday"
// Friday

day = 1000
// error: type mismatch
```

```kotlin
val b: Byte =  1
val i: Int = b
// error: ype mismatch

val i: Int = b.toInt()
// 1
```


Tidak boleh `null`

```kotlin
var rock: Int = null
// error: null cannot be a value of a non-null type Int
```

Jika ingin nilainya `null` maka gunakan tanda `?`

```kotlin
var marble: Int? = null

var listOfFish: List<String?> = listOf(null, null)

var everMoreFish: List<String>? = null
```

## String

Kamu dapat melakukan concat string dengan tanda `+`

```kotlin
"Kucing " + "Jantan"
```

Kamu juga dapat menggunakan string template

```kotlin
val age: Int = 21
val name: String = "Anis Fikriyyah"

"My name is $name and now I am ${age + 3} years old"
```

```kotlin
"ayam" == "ikan"
// false
```

```kotlin
val rangers = 30
if (rangers in 1..100) println(rangers)
// 30
```

```kotlin
when(rangers) {
    0 -> println("Nol")
    30 -> println("Tiga Puluh")
    50 -> println("Lima Puluh")
    else -> println("Kebanyakan") 
}
// Tiga Puluh
```

```kotlin
var name = "Anis Fikriyyah"
name.length
// 14
```

## Array

```kotlin
val myList = mutableListOf("tuna", "salmon", "shark")
myList = mutableListOf("koi", "goldfish")
// error: val cannot be reassigned
```

```kotlin
val myList = mutableListOf("tuna", "salmon", "shark")
myList.remove("shark")
// true
```

```kotlin
import java.util.*

val mix = arrayOf("fish", 2)
Array.toString(mix)
// [fish, 2]
```

```kotlin
val array = Array(5) { it * 2 }
array.asList()
// [ 0, 2, 4, 6, 8 ]
```

```kotlin
for ( i in 'b'..'g') println(i)
// bcdefg

for ( i in 1..10 ) println(i)
// 12345678910
```

-----

## Kotlin file

Jika ingin menggunakan file kotlin harus ada fun `main`

```kotlin
fun main(args: Array<String>) {
    println("Hello Anis")
}
```
