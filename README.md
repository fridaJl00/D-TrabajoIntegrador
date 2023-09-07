Algoritmo VentasEntradasConciertoHarryStyles
	
	// Variables
	Definir cantidadEntradasTotales, cantidadEntradasVendidas, cantidadEntradasDisponibles Como Entero
	Definir precioEntrada Como Real
	Definir nombreCliente, apellidoCliente, emailCliente Como Cadena
	
	// Inicio
	
	// Inicializa variables
	cantidadEntradasTotales = 10000
	cantidadEntradasVendidas = 0
	cantidadEntradasDisponibles = cantidadEntradasTotales - cantidadEntradasVendidas
	precioEntrada = 100
	
	// Menú principal
	
	Escribir "Bienvenido al sistema de ventas de entradas para el concierto de Harry Styles"
	Escribir "¿Qué desea hacer?"
	Escribir "1. Comprar entradas"
	Escribir "2. Ver disponibilidad de entradas"
	Escribir "3. Salir"
	Leer opcionMenu
	
	// Compra de entradas
	
	Mientras opcionMenu = 1 Hacer
		
		// Solicita información al cliente
		Escribir "Ingrese su nombre:"
		Leer nombreCliente
		Escribir "Ingrese su apellido:"
		Leer apellidoCliente
		Escribir "Ingrese su correo electrónico:"
		Leer emailCliente
		Escribir "¿Cuántas entradas desea comprar?"
		Leer cantidadEntradas
		
		// Valida que haya entradas disponibles
		Si cantidadEntradas > cantidadEntradasDisponibles Entonces
			Escribir "No hay suficientes entradas disponibles"
		SiNo
			// Calcula el precio total de las entradas
			precioTotal = cantidadEntradas * precioEntrada
			// Actualiza la cantidad de entradas vendidas
			cantidadEntradasVendidas = cantidadEntradasVendidas + cantidadEntradas
			// Actualiza la cantidad de entradas disponibles
			cantidadEntradasDisponibles = cantidadEntradasDisponibles - cantidadEntradas
			// Imprime el recibo de la venta
			Escribir "Recibo de venta"
			Escribir "Cliente:"
			Escribir nombreCliente, apellidoCliente
			Escribir "Correo electrónico:"
			Escribir emailCliente
			Escribir "Entradas vendidas:"
			Escribir cantidadEntradas
			Escribir "Precio total:"
			Escribir precioTotal
		Fin Si
		
		// Pregunta si desea comprar más entradas
		Escribir "¿Desea comprar más entradas? (1: Sí / 0: No)"
		Leer opcionMenu
		
	Fin Mientras
	
	// Ver disponibilidad de entradas
	
	Si opcionMenu = 2 Entonces
		
		// Imprime la cantidad de entradas disponibles
		Escribir "La cantidad de entradas disponibles es de", cantidadEntradasDisponibles
		
	Fin Si
	
	// Salir del sistema
	
	Si opcionMenu = 3 Entonces
		
		Escribir "¡Gracias por usar nuestro sistema!"
		
	Fin Si
	
FinAlgoritmo
