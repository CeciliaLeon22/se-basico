Python 3.11.0 (main, Oct 24 2022, 18:26:48) [MSC v.1933 64 bit (AMD64)] on win32
Type "help", "copyright", "credits" or "license" for more information.
>>>
>>> # Definir la base de conocimiento
>>> base_de_conocimiento = {
...     'sintoma1': 'enfermedad1',
...     'sintoma2': 'enfermedad2',
...     'sintoma3': 'enfermedad3',
...     # Agrega más reglas aquí
... }
>>>
>>> # Función para el motor de inferencia
>>> def motor_de_inferencia(sintomas):
...     for sintoma, enfermedad in base_de_conocimiento.items():
...         if all(sintoma in sintomas for sintoma in sintoma.split(',')):
...             return enfermedad
...     return 'Enfermedad desconocida'
...
>>> # Entrada del usuario
>>> sintomas = input("Ingresa los síntomas (separados por comas): ").split(',')
Ingresa los síntomas (separados por comas):
>>> # Realizar la inferencia
>>> enfermedad_diagnosticada = motor_de_inferencia(sintomas)
>>>
>>> # Mostrar el resultado
>>> print(f"El sistema experto diagnosticó: {enfermedad_diagnosticada}")
