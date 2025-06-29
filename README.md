# Clase Empleado para gestionar datos de un empleado

class Empleado:
    # Constructor que inicializa los atributos del empleado
    def __init__(self, nombre, edad, puesto, salario):
        self.nombre = nombre
        self.edad = edad
        self.puesto = puesto
        self.salario = salario

    # Método para aumentar el salario
    def aumentar_salario(self, porcentaje):
        self.salario += self.salario * (porcentaje / 100)

    # Método para mostrar la información del empleado
    def mostrar_informacion(self):
        print(f"Nombre: {self.nombre}")
        print(f"Edad: {self.edad}")
        print(f"Puesto: {self.puesto}")
        print(f"Salario: ${self.salario:.2f}")


# Programa principal para probar la clase Empleado
if __name__ == "__main__":
    # Instanciación de objetos
    empleado1 = Empleado("Carlos Martínez", 30, "Analista", 45000)
    empleado2 = Empleado("Lucía Gómez", 28, "Desarrolladora", 52000)

    # Uso de métodos
    empleado1.aumentar_salario(10)  # Aumentar 10%
    empleado2.aumentar_salario(5)   # Aumentar 5%

    # Mostrar información actualizada
    print("=== Información del Empleado 1 ===")
    empleado1.mostrar_informacion()

    print("\n=== Información del Empleado 2 ===")
    empleado2.mostrar_informacion()
