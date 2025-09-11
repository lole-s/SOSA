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

| Dec |   Char  | Dec | Char | Dec | Char | Dec | Char |     |
| --: | :-----: | --: | :--: | --: | :--: | --: | :--: | --- |
|   0 |   NUL   |   1 |  SOH |   2 |  STX |   3 |  ETX |     |
|   4 |   EOT   |   5 |  ENQ |   6 |  ACK |   7 |  BEL |     |
|   8 |    BS   |   9 |  TAB |  10 |  LF  |  11 |  VT  |     |
|  12 |    FF   |  13 |  CR  |  14 |  SO  |  15 |  SI  |     |
|  16 |   DLE   |  17 |  DC1 |  18 |  DC2 |  19 |  DC3 |     |
|  20 |   DC4   |  21 |  NAK |  22 |  SYN |  23 |  ETB |     |
|  24 |   CAN   |  25 |  EM  |  26 |  SUB |  27 |  ESC |     |
|  28 |    FS   |  29 |  GS  |  30 |  RS  |  31 |  US  |     |
|  32 |  Space  |  33 |  `!` |  34 |  `"` |  35 |  `#` |     |
|  36 |   `$`   |  37 |  `%` |  38 |  `&` |  39 |  `'` |     |
|  40 |   `(`   |  41 |  `)` |  42 |  `*` |  43 |  `+` |     |
|  44 |   `,`   |  45 |  `-` |  46 |  `.` |  47 |  `/` |     |
|  48 |   `0`   |  49 |  `1` |  50 |  `2` |  51 |  `3` |     |
|  52 |   `4`   |  53 |  `5` |  54 |  `6` |  55 |  `7` |     |
|  56 |   `8`   |  57 |  `9` |  58 |  `:` |  59 |  `;` |     |
|  60 |   `<`   |  61 |  `=` |  62 |  `>` |  63 |  `?` |     |
|  64 |   `@`   |  65 |  `A` |  66 |  `B` |  67 |  `C` |     |
|  68 |   `D`   |  69 |  `E` |  70 |  `F` |  71 |  `G` |     |
|  72 |   `H`   |  73 |  `I` |  74 |  `J` |  75 |  `K` |     |
|  76 |   `L`   |  77 |  `M` |  78 |  `N` |  79 |  `O` |     |
|  80 |   `P`   |  81 |  `Q` |  82 |  `R` |  83 |  `S` |     |
|  84 |   `T`   |  85 |  `U` |  86 |  `V` |  87 |  `W` |     |
|  88 |   `X`   |  89 |  `Y` |  90 |  `Z` |  91 |  `[` |     |
|  92 |   `\`   |  93 |  `]` |  94 |  `^` |  95 |  `_` |     |
|  96 | `` ` `` |  97 |  `a` |  98 |  `b` |  99 |  `c` |     |
| 100 |   `d`   | 101 |  `e` | 102 |  `f` | 103 |  `g` |     |
| 104 |   `h`   | 105 |  `i` | 106 |  `j` | 107 |  `k` |     |
| 108 |   `l`   | 109 |  `m` | 110 |  `n` | 111 |  `o` |     |
| 112 |   `p`   | 113 |  `q` | 114 |  `r` | 115 |  `s` |     |
| 116 |   `t`   | 117 |  `u` | 118 |  `v` | 119 |  `w` |     |
| 120 |   `x`   | 121 |  `y` | 122 |  `z` | 123 |  `{` |     |
| 124 |    \`   |  \` |  125 | `}` |  126 | `~` |  127 | DEL |

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

## 5. Cierre (5 min)

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
