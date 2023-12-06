#Saludos en Go

Este paquete proporciona una forma simple de obtener saludos personalizados en Go

## Instalación
Ejecutar el siguiente comando para instalar el paquete:
```bash
go get -u github.com/bodoky/greetings 
```

## Uso

Aqui tienes un ejemplo de uso del paquete 

```go
package main

import (
	"fmt"
	"log"

	"github.com/bodoky/greetings"
)

func main() {

	log.SetPrefix("greetings: ")
	log.SetFlags(0)

	names := []string{"Marco", "Juan", "Pedro"}
	messages, err := greetings.Hellos(names)

	//message, err := greetings.Hello("JORGE")

	if err != nil {
		log.Fatal(err)
	}
	fmt.Println(messages)
}

```
Este ejemplo importa el paquete  github.com/bodoky/greetings y llama a la función Hellos para mostrar  saludos personalizados