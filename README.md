# Parcial 1 - Lenguajes de Programación  
**Repositorio con soluciones a 5 problemas prácticos de análisis léxico, sintáctico y rendimiento.**

---

## 📋 Contenido  
1. [Pregunta 1: Analizador Léxico en AWK](#pregunta-1)  
2. [Pregunta 2: Validador de Expresiones Lambda en LEX](#pregunta-2)  
3. [Pregunta 3: Contador de Palabras en C](#pregunta-3)  
4. [Pregunta 4: Comparación de Rendimiento (C vs. Python)](#pregunta-4)  
5. [Pregunta 5: Calculadora de Números Complejos con ANTLR](#pregunta-5)  

---

## ⚙️ Requisitos  
- **Sistema Operativo**: Linux/Ubuntu (recomendado).  
- **Herramientas**:  
  - `gawk`, `flex`, `gcc`, `python3`, `antlr4`.  
- **Instalación de dependencias**:  
  ```bash
  sudo apt-get install gawk flex gcc python3 antlr4
  pip3 install antlr4-python3-runtime numpy
Pregunta 1
Analizador Léxico en AWK

Descripción: Clasifica tokens (enteros, reales, +, ++) desde un archivo de texto.
Archivos:

    token.awk: Script de AWK.

    token.txt: Ejemplo de entrada.

Ejecución:
gawk -f token.awk token.txt
Pregunta 2
Validador de Expresiones Lambda en LEX

Descripción: Verifica sintaxis de expresiones lambda de Python.
Archivos:

    lambda.l: Reglas LEX.

    archivo.txt: Ejemplo válido.

    archivo_no_acepta.txt: Ejemplo inválido.

Compilación y ejecución:
flex lambda.l
gcc lex.yy.c -o lambda -lfl
./lambda archivo.txt          # ACEPTA
./lambda archivo_no_acepta.txt # NO ACEPTA
Pregunta 3
Contador de Palabras en C

Descripción: Cuenta ocurrencias de una palabra en un archivo.
Archivos:

    contador.c: Código fuente.

    texto.txt: Ejemplo de texto.

Ejecución:
gcc contador.c -o contador
./contador texto.txt arroz

pregunta 4
Análisis del Impacto de la Branch Prediction en Bucles
Descripción  
Este ejercicio compara el rendimiento de bucles con condiciones **predecibles** (datos ordenados) e **impredecibles** (datos aleatorios) en C (lenguaje compilado) y Python (lenguaje interpretado). El objetivo es demostrar cómo la *branch prediction* del CPU afecta el rendimiento en cada caso.
archivos:
    predecible.c: Código C con datos ordenados.

    impredecible.c: Código C con datos aleatorios.

    predecible_e_impredecible.py: Script Python con ambas versiones.
ejecucion:
# Compilar y ejecutar en C  
gcc -O3 branch_predecible.c -o predecible && ./predecible  
gcc -O3 branch_impredecible.c -o impredecible && ./impredecible  

# Ejecutar en Python  
python3 branch.py  

Pregunta 5
Calculadora de Números Complejos con ANTLR

Descripción: Evalúa operaciones con números complejos (+, -, *, /).
Archivos:

    Complex.g4: Gramática ANTLR.

    main.py: Programa principal.

Ejecución:
antlr4 -Dlanguage=Python3 Complex.g4
python3 main.py input.txt

Solución de Problemas

    Error en ANTLR: Asegúrate de renombrar el visitor personalizado a CustomVisitor.py.

    Fallo en LEX: Verifica que los paréntesis estén balanceados en las expresiones lambda.
