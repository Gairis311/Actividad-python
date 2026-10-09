carreras: tuple[str, ...] = ("Ingeniería de Software", "Contabilidad", "Derecho")

personas: list[tuple[str, str, int, int]] = [
    # nombre, apellido, edad, carrera
]

estudiantes: list[dict[str, str | int]] = [
    # Lista de diccionario con nombre, apellido, edad, carrera
]

for _ in range(5):
    nombre = input("Ingrese su nombre: ")
    apellido = input("Ingrese su apellido: ")
    edad = int(input("Ingrese su edad: "))
    carrera = int(input("Seleccione su carrera (0, 1 o 2): "))

    persona = (nombre, apellido, edad, carrera)
    personas.append(persona)

for persona in personas:
    nombre = persona[0]
    apellido = persona[1]
    edad = persona[2]
    indice_carrera = persona[3]

    nombre_carrera = carreras[indice_carrera]

    estudiante = {
        "nombre": nombre,
        "apellido": apellido,
        "edad": edad,
        "carrera": nombre_carrera
    }

    estudiantes.append(estudiante)

for estudiante in estudiantes:
    print(
        estudiante["nombre"], estudiante["apellido"],
        "tiene", estudiante["edad"], "años y estudia",
        estudiante["carrera"]
    )
