[![VS Code Marketplace](https://img.shields.io/badge/VS%20Code%20Marketplace-Octave%20Snippets%20Enhanced-blue)](https://marketplace.visualstudio.com/items?itemName=ramonseg89-spec.octave-snippets-enhanced)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)
[![GitHub stars](https://img.shields.io/github/stars/ramonseg89-spec/octave-vscode-snippets)](https://github.com/ramonseg89-spec/octave-vscode-snippets/stargazers)

# Octave Snippets Enhanced

**Más de 100 snippets para GNU Octave 8.4.0** – escribe código más rápido en VS Code.  
Sintaxis 100% compatible con Octave (usa `endfor`, `endif`, `endfunction`, `end_try_catch`, etc.).

---

## 📦 Instalación

### Desde el Marketplace de VS Code (recomendado)
1. Abre VS Code.
2. Ve a Extensiones (`Ctrl+Shift+X`).
3. Busca `Octave Snippets Enhanced`.
4. Haz clic en **Instalar**.

### Manual (si no usas Marketplace)
1. Copia el contenido de [`snippets/octave.json`](./snippets/octave.json).
2. En VS Code: `Ctrl+Shift+P` → **Configure User Snippets** → selecciona `octave.json`.
3. Pega el contenido y guarda.

---

## 📑 Snippets incluidos (más de 100)

> **Navegación con TAB**: todos los snippets tienen placeholders `${1:...}`, `${2:...}`. Presiona `TAB` para moverte entre ellos. El cursor termina en `$0`.

### 🔁 Control de flujo
| Prefix | Descripción | Palabra clave de cierre |
|--------|-------------|--------------------------|
| `for`   | Bucle for básico (`start:end`) | `endfor` |
| `fors`  | Bucle for con paso (`start:step:end`) | `endfor` |
| `forn`  | Bucles for anidados | `endfor` |
| `forb`  | For con `break` condicional | `endfor` |
| `while` | Bucle while | `endwhile` |
| `whilec`| While con contador explícito | `endwhile` |
| `do`    | Bucle do-until | `until` |
| `if`    | If simple | `endif` |
| `ife`   | If-else | `endif` |
| `ifee`  | If-elseif-else | `endif` |
| `ifeee` | If con dos o más elseif | `endif` |
| `switch`| Switch-case-otherwise | `endswitch` |
| `try`   | Try-catch (manejo de errores) | `end_try_catch` |
| `uwp`   | `unwind_protect` (limpieza garantizada, exclusivo de Octave) | `end_unwind_protect` |

### 📐 Funciones
| Prefix | Descripción |
|--------|-------------|
| `fun`   | Función con un valor de retorno |
| `funm`  | Función con múltiples retornos |
| `funv`  | Función void (sin retorno) |
| `anon`  | Función anónima: `f = @(x) x.^2` |

### 📊 Gráficos

#### 2D básico y avanzado
| Prefix | Descripción |
|--------|-------------|
| `plot`   | Gráfico básico con etiquetas y grid |
| `plots`  | Gráfico con estilo de línea y leyenda |
| `scatter`| Diagrama de dispersión con puntos rellenos |
| `bar`    | Barras verticales |
| `barh`   | Barras horizontales |
| `hist`   | Histograma |
| `stairs` | Gráfico escalonado |
| `stem`   | Gráfico de tallos |
| `area`   | Área rellena bajo la curva |
| `pie`    | Gráfico de pastel |
| `boxplot`| Diagrama de caja (*requiere `pkg load statistics`*) |
| `errorbar`| Línea con barras de error |
| `fill`   | Relleno de polígono |

#### Escalas logarítmicas
| Prefix | Descripción |
|--------|-------------|
| `loglog`    | Ambos ejes en escala logarítmica |
| `semilogx`  | Eje X logarítmico |
| `semilogy`  | Eje Y logarítmico |

#### 3D y campos vectoriales
| Prefix | Descripción |
|--------|-------------|
| `contour` | Gráfico de contorno 2D |
| `surf`    | Superficie 3D con shading |
| `mesh`    | Malla 3D wireframe |
| `plot3`   | Línea 3D con ángulo de vista |
| `quiver`  | Campo de vectores 2D |

### 🧮 Vectores, matrices y álgebra lineal
| Prefix | Descripción |
|--------|-------------|
| `vec`    | Vector fila `[1, 2, 3]` |
| `vecc`   | Vector columna `[1; 2; 3]` |
| `lsp`    | `linspace` |
| `logspace`| Vector logarítmico |
| `meshgrid`| Grilla 2D para 3D/contornos |
| `mat`    | Matriz con valores |
| `matz`   | Matriz de ceros |
| `mato`   | Matriz de unos |
| `mati`   | Matriz identidad |
| `repmat` | Repetir matriz/vector |
| `reshape`| Cambiar dimensiones |
| `roots`  | Raíces de polinomio |
| `polyval`| Evaluar polinomio |
| `polyfit`| Ajuste polinomial |
| `solve`  | Sistema lineal `A \ b` |
| `inv`    | Inversa (mejor usar `\`) |
| `det`    | Determinante |
| `eig`    | Valores/vectores propios |
| `svd`    | Descomposición SVD |
| `norm`   | Norma vector/matriz |
| `cond`   | Número de condición |

### 📈 Matemáticas avanzadas
| Prefix | Descripción |
|--------|-------------|
| `interp1` | Interpolación 1D |
| `interp2` | Interpolación 2D |
| `trapz`   | Integral trapezoidal |
| `diff`    | Derivada numérica |
| `gradient`| Gradiente numérico |

### 🗂️ Estructuras de datos
| Prefix | Descripción |
|--------|-------------|
| `cell`     | Crear cell array vacío |
| `cellidx`  | Asignar valor a celda |
| `struct`   | Crear campo en estructura |
| `structarray` | Array de estructuras |
| `cellfun`  | Aplicar función a cell array |
| `arrayfun` | Aplicar función a array numérico |
| `structfun`| Aplicar función a campos de struct |

### 🛠️ Utilidades generales
| Prefix | Descripción |
|--------|-------------|
| `find`    | Índices donde se cumple condición |
| `unique`  | Valores únicos |
| `ismember`| Pertenencia a conjunto |
| `sort`    | Ordenamiento con índices |
| `stats`   | Bloque: sum, mean, median, std, var |
| `cumsum`  | Suma acumulada |
| `cumprod` | Producto acumulado |
| `main`    | Script principal (clc, clear, close all + secciones) |
| `header`  | Inicialización limpia |
| `cb`      | Separador de sección `%% --- ... ---` |
| `doc`     | Bloque de documentación (autor, fecha, desc.) |
| `pf`      | `printf` simple |
| `pfm`     | `printf` múltiple |
| `fw`      | `fprintf` con formato de tabla (consola) |
| `fwf`     | `fprintf` a archivo con formato de tabla |

### 🎨 Colores
| Prefix | Resultado |
|--------|-----------|
| `red`, `green`, `blue`, `cyan`, `magenta`, `yellow`, `black`, `white` | `'r'`, `'g'`, `'b'`, `'c'`, `'m'`, `'y'`, `'k'`, `'w'` |
| `rgb`   | `[0.5, 0.2, 0.8]` (valores entre 0 y 1) |

---

## 💡 Ejemplos destacados

### Función anónima (`anon`)
```
f = @(x) x.^2;
```
Útil para `arrayfun`, `cellfun`, `fzero`, etc.

### Superponer gráficas (`hold`)
```
hold on;
plot(x1, y1, 'b-');
plot(x2, y2, 'r--');
hold off;
```

### Manejo de errores con limpieza garantizada (`uwp`)
```
unwind_protect
    % código que puede fallar
unwind_protect_cleanup
    % siempre se ejecuta (con o sin error)
end_unwind_protect
```

### Búsqueda de raíces (`fzero`)
```
f = @(x) x.^2 - 2;
x0 = 1;
raiz = fzero(f, x0);
```

### Formato de tabla con `fprintf` (`fw`)
```
fprintf('%-15s %10.4f\n', 'Valor', 3.14159);
```

---

## ⚠️ Diferencias clave Octave vs MATLAB

| Construcción | Octave | MATLAB |
|--------------|--------|--------|
| Fin de `for` | `endfor` | `end` |
| Fin de `while` | `endwhile` | `end` |
| Fin de `if` | `endif` | `end` |
| Fin de `switch` | `endswitch` | `end` |
| Fin de función | `endfunction` | `end` (opcional) |
| Fin de try‑catch | `end_try_catch` | `end` |
| `do-until` | ✅ nativo | ❌ no existe |
| `unwind_protect` | ✅ nativo | ❌ no existe |

> **Nota:** Octave acepta `end` genérico, pero usar las palabras clave específicas mejora la legibilidad y los mensajes de error.

---

## 🤝 Contribuir

¿Falta algún snippet que uses a menudo? ¿Encontraste un error?  
Lee [`CONTRIBUTING.md`](./CONTRIBUTING.md) para saber cómo añadir nuevos snippets o reportar problemas.

---

## 📄 Licencia

MIT – ver archivo [LICENSE](LICENSE).

---

## 🌟 ¡Gracias por usar Octave Snippets Enhanced!

Si te resulta útil, considera darle una ⭐ en [GitHub](https://github.com/ramonseg89-spec/octave-vscode-snippets) y compartirlo con la comunidad de Octave.
