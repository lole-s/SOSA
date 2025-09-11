# Clase práctica: **¿Cómo entienden las computadoras las letras y símbolos?**

## 🎯 Objetivos

* Comprender que la información en la computadora se representa con números binarios.
* Conocer qué es el **código ASCII** y cómo representa letras y símbolos.
* Explorar el **código Unicode** y su importancia para otros idiomas y emojis.

---

## Introducción (5 min) - Tablas de codificación de caracteres

  ```
  01001000 01101111 01101100 01100001
  ```

 **¿Qué creen que dice?**

* Las computadoras no entienden letras, solo **números (binario)**.
* Lon números anteriores representan “Hola” usando un código especial: **ASCII**.

---

## Actividad práctica 1: ASCII (10 min)

1. Usando una **tabla ASCII simplificada** (solo letras A–Z, a–z, números y algunos símbolos).
2. En parejas:

   * Conviertan su **nombre** en código ASCII decimal (ej: “Ana” → 65 110 97).
   * Opcional: en binario (ej: 65 → 01000001).

---

# 📋 Tabla ASCII (0–127)

| Dec | Char  | Dec | Char | Dec | Char |
| --- | ----- | --- | ---- | --- | ---- |
| 0   | NUL   | 43  | +    | 86  | V    |
| 1   | SOH   | 44  | ,    | 87  | W    |
| 2   | STX   | 45  | -    | 88  | X    |
| 3   | ETX   | 46  | .    | 89  | Y    |
| 4   | EOT   | 47  | /    | 90  | Z    |
| 5   | ENQ   | 48  | 0    | 91  | \[   |
| 6   | ACK   | 49  | 1    | 92  | \\   |
| 7   | BEL   | 50  | 2    | 93  | ]    |
| 8   | BS    | 51  | 3    | 94  | ^    |
| 9   | TAB   | 52  | 4    | 95  | \_   |
| 10  | LF    | 53  | 5    | 96  | \`   |
| 11  | VT    | 54  | 6    | 97  | a    |
| 12  | FF    | 55  | 7    | 98  | b    |
| 13  | CR    | 56  | 8    | 99  | c    |
| 14  | SO    | 57  | 9    | 100 | d    |
| 15  | SI    | 58  | :    | 101 | e    |
| 16  | DLE   | 59  | ;    | 102 | f    |
| 17  | DC1   | 60  | <    | 103 | g    |
| 18  | DC2   | 61  | =    | 104 | h    |
| 19  | DC3   | 62  | >    | 105 | i    |
| 20  | DC4   | 63  | ?    | 106 | j    |
| 21  | NAK   | 64  | @    | 107 | k    |
| 22  | SYN   | 65  | A    | 108 | l    |
| 23  | ETB   | 66  | B    | 109 | m    |
| 24  | CAN   | 67  | C    | 110 | n    |
| 25  | EM    | 68  | D    | 111 | o    |
| 26  | SUB   | 69  | E    | 112 | p    |
| 27  | ESC   | 70  | F    | 113 | q    |
| 28  | FS    | 71  | G    | 114 | r    |
| 29  | GS    | 72  | H    | 115 | s    |
| 30  | RS    | 73  | I    | 116 | t    |
| 31  | US    | 74  | J    | 117 | u    |
| 32  | (esp) | 75  | K    | 118 | v    |
| 33  | !     | 76  | L    | 119 | w    |
| 34  | "     | 77  | M    | 120 | x    |
| 35  | #     | 78  | N    | 121 | y    |
| 36  | \$    | 79  | O    | 122 | z    |
| 37  | %     | 80  | P    | 123 | {    |
| 38  | &     | 81  | Q    | 124 | \|   |
| 39  | '     | 82  | R    | 125 | }    |
| 40  | (     | 83  | S    | 126 | \~   |
| 41  | )     | 84  | T    | 127 | DEL  |
| 42  | \*    | 85  | U    |     |      |

---

👉 Observaciones:

* De **0 a 31** y el **127** son **caracteres de control** (no imprimibles), por eso aparecen con abreviaturas (NUL, TAB, CR, ESC, DEL…).
* De **32 a 126** son visibles: espacios, números, letras, símbolos.

---

👉 Herramienta online de apoyo: [https://www.asciitable.com/](https://www.asciitable.com/)

---




## Actividad práctica 2: Unicode (10 min)

* Pregunta: **¿Y cómo escribimos una ñ, un símbolo chino o un emoji?**
* ASCII se queda corto (solo 128 símbolos).
* **Unicode** amplía el repertorio (letras de todos los idiomas + emojis).

🔹 Actividad:

* Texto con símbolos de distintos idiomas y emojis:

  ```
  ¡Hola! 😀 你好 Привет
  ```
* Usar el convertidor online para ver los **códigos Unicode** de cada carácter:
  👉 [https://unicodelookup.com/](https://unicodelookup.com/)
* ¿cuál usa más “números”?

---

## Actividad práctica 3: Programita rápido (10 min)

Si hay Python:

```python
texto = input("Escribí una palabra: ")
for letra in texto:
    print(letra, "->", ord(letra))
```

* Escriben palabras y ven los **códigos ASCII/Unicode** de cada carácter.
* Pueden probar con letras normales, tildes y emojis.

---

## 5. Cierre y reflexión (5 min)

* Preguntar:

  * ¿Por qué creen que Unicode es importante hoy en día?
  * ¿Qué pasaría si solo tuviéramos ASCII?
* Conclusión:

  * **ASCII** → los primeros pasos (inglés).
  * **Unicode** → el mundo entero (todos los idiomas + símbolos modernos).

* ASCII: 7 bits (128 símbolos). 1963
* ASCII extendido: 8 bits (256 símbolos). Entre 1970 y 1980
* Unicode (UTF-8): entre 8 y 32 bits (más de 140.000 símbolos). 1991

---
