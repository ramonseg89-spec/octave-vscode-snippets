# Octave Snippets Enhanced

32 snippets esenciales para GNU Octave 8.4.0 en VS Code. Sintaxis verificada contra la [documentación oficial de Octave 8.4.0](https://docs.octave.org/v8.4.0/).

## Instalación

### Opción A — Manual (recomendada mientras no está en Marketplace)

1. Abre VS Code
2. `Ctrl+Shift+P` → **Open User Snippets**
3. Escribe `octave` → selecciona o crea `octave.json`
4. Pega el contenido de `snippets/octave.json`

### Opción B — Como extensión local

```bash
git clone https://github.com/TU-USUARIO-GITHUB/octave-vscode-snippets
cd octave-vscode-snippets
# Copiar snippets/octave.json al directorio de snippets de VS Code
```

### Opción C — VS Code Marketplace *(próximamente)*

Busca **"Octave Snippets Enhanced"** en el Marketplace.

---

## Snippets disponibles

### Control de flujo

| Prefix | Descripción | Cierre Octave |
|--------|-------------|---------------|
| `for` | Bucle for básico `start:end` | `endfor` |
| `fors` | Bucle for con paso `start:step:end` | `endfor` |
| `forn` | Bucles for anidados | `endfor` |
| `while` | Bucle while | `endwhile` |
| `do` | Bucle do-until (ejecuta al menos una vez) | `until` |
| `if` | If simple | `endif` |
| `ife` | If-else | `endif` |
| `ifee` | If-elseif-else | `endif` |
| `ifi` | Ternario inline (aritmética lógica) | — |
| `switch` | Switch-case-otherwise | `endswitch` |
| `try` | Try-catch | `end_try_catch` |

### Funciones

| Prefix | Descripción |
|--------|-------------|
| `fun` | Función con un valor de retorno |
| `funm` | Función con múltiples retornos |
| `funv` | Función void (sin retorno) |

### Vectores y matrices

| Prefix | Descripción |
|--------|-------------|
| `vec` | Vector fila `[1, 2, 3]` |
| `vecc` | Vector columna `[1; 2; 3]` |
| `lsp` | Vector linspace uniforme |
| `mat` | Matriz con valores |
| `matz` | Matriz de ceros |
| `mato` | Matriz de unos |
| `mati` | Matriz identidad |

### Gráficos

| Prefix | Descripción |
|--------|-------------|
| `plot` | Gráfico básico con etiquetas y grid |
| `plots` | Gráfico con estilo de línea y leyenda |
| `subplot` | Subgráfico dentro de una figura |
| `fig` | Figura personalizada con FontSize y axis tight |

### Salida y utilidades

| Prefix | Descripción |
|--------|-------------|
| `pf` | `printf` con una variable |
| `pfm` | `printf` con múltiples variables |
| `disp` | `disp()` para mostrar variable |

### Estructura de script

| Prefix | Descripción |
|--------|-------------|
| `main` | Script principal con secciones (clc, clear, close all) |
| `header` | Inicialización limpia (clc, clear, close all) |
| `cb` | Separador de sección `%% --- Titulo ---` |
| `doc` | Bloque de documentación opcional (autor, fecha, desc) |

---

## Diferencias clave Octave vs MATLAB

Estos snippets usan sintaxis **específica de Octave**, no compatible con MATLAB:

| Construcción | Octave | MATLAB |
|---|---|---|
| Fin de `for` | `endfor` | `end` |
| Fin de `while` | `endwhile` | `end` |
| Fin de `if` | `endif` | `end` |
| Fin de `switch` | `endswitch` | `end` |
| Fin de función | `endfunction` | `end` (opcional) |
| Fin de try-catch | **`end_try_catch`** | `end` |
| `do-until` | ✅ nativo | ❌ no existe |

> **Nota:** Octave acepta `end` genérico, pero los keywords específicos dan mejores mensajes de diagnóstico.

---

## Ejemplo de uso

Escribe `for` + Tab:

```octave
for i = 1:n
    % cuerpo del bucle
endfor
```

Escribe `main` + Tab:

```octave
clc;
clear;
close all;

%% --- Parametros ---
% tus variables aqui

%% --- Procesamiento ---

%% --- Resultados ---
% muestra resultados
```

Escribe `try` + Tab:

```octave
try
    % codigo que puede fallar
catch err
    printf('Error: %s\n', err.message);
end_try_catch
```

---

## Contribuir

Ver [CONTRIBUTING.md](CONTRIBUTING.md).

## Licencia

MIT — ver [LICENSE](LICENSE).
