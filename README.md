[miprimernegocio (1).py](https://github.com/user-attachments/files/29652960/miprimernegocio.1.py)
# mi-primer-negocio-
mi primer negocio 
#perfumeria_urban_nex 
def menu(opcion):
        if opcion == 1:
            print("MIRA EL CATALOGO QUE TENEMOS PARA TI:")
            print("1. Nautica voyage: el rey de la frescura economica huele a manzanas verdes $10")
            print("2. Club de nuit intense man: famoso por ser el clon mas cercano a opciones de lujo es potente amaderado y muy duradero $15")
            print("3. Halloween man x: una opcion moderna con notas de cafe y whisky perfecta para salidas nocturnas informales $14")
        elif opcion == 2:
            print("MIRA ESTO TE PUEDE GUSTAR:")
            print("1. Iorgio armani: una evolucion moderna del clasico mas intensa mineral y con un azul profundo muy elegante 25$")
            print("2. Suavague: probablemente el perfume mas versatil del mundo es especiado fresco y tiene una proyeccion masiva 30$")
            print("3. Blue de chanel: la definicion de perfume azul sofisticado es equilibrado profesional y extremadamente pulcro 30$")
        elif opcion == 3:
            print("El lujo lo posees en la mano")
            print("1. Aventus: un icono del lujo mezcla notas de piña abedul y almizcle es el estandar de oro para muchos coleccionistas 90$") 
            print("2. Boccarat rougue 540: una fragancia que se siente como oro liquido es dulce resinosa y tiene un aura sofisticada inigualable 100$")
            print("3. Layton Parfums de Marly: una combinacion magistral de vainilla manzana y pimienta que grita opulencia y buen gusto 150$")
def obtener_precio(categoria, producto):
        if categoria == 1:
            if producto == 1:
                return 10
            elif producto == 2:
                return 15
            elif producto == 3:
                return 14

        elif categoria == 2:
            if producto == 1:
                return 25
            elif producto == 2:
                return 30
            elif producto == 3:
                return 30
        
        elif categoria == 3:
            if producto == 1:
                return 90
            elif producto == 2:
                return 100
            elif producto == 3:
                return 150
        return 0
def calcular_total(*precios):
    return sum(precios)

def factura(**datos):
    total = datos["total"]

    print("TOTAL A PAGAR: $", total)
    nombre = input("INGRESE SU NOMBRE PARA LA FACTURA: ")
    print("MUCHAS GRACIAS", nombre)

    print("AHORA SU METODO DE PAGO")
    print("1. TRANSFERENCIA")
    print("2. EFECTIVO")

    dinero = int(input("ELIJA EL METODO DE PAGO: "))

    if dinero == 1:
        cedula = input("DIGITE SU NUMERO DE CEDULA: ")
        correo = input("INGRESE SU CORREO: ")
        telefono = input("INGRESE SU TELEFONO: ")

    elif dinero == 2:
        nombres = input("DIGITE SUS NOMBRES COMPLETOS: ")
        print("MUCHAS GRACIAS", nombres)

    print("GRACIAS POR SU COMPRA EN URBAN NEX")
    print("-----------------------------------")
    print("RECUERDA QUE")
    print("CADA PEQUEÑO ESFUERZO DE HOY TE ACERCA A UNA GRAN META MAÑANA")
    print("QUE TENGA UN GRAN DIA")
    print("-----------------------------------")  

op = "si"
total = 0

while op == "si" or op == "SI":
    print("-------------BIENVENIDO-----------")
    print("DESCUBRE LAS MEJORES FRAGANCIAS PARA HOMBRES Y MUJERES")
    print("----- 1. PERFUMES ECONOMICOS")
    print("----- 2. PERFUMES ESTANDAR")
    print("----- 3. PERFUMES DE LUJO")

    opcion = int(input("ESCOJA LA CATEGORIA QUE DESEE SELECCIONE EL NUMERO: "))

    menu(opcion)

    producto = int(input("ELIJA EL PERFUME QUE LE GUSTE : "))

    precio = obtener_precio(opcion, producto)

    total = calcular_total(total, precio)

    print("SUBTOTAL: $", total)

    op = input("QUIERE OTRO PERFUME SI O NO : ")

factura(total=total)
