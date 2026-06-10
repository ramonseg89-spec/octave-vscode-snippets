# Contribuir a Octave Snippets Enhanced

## Cómo añadir un snippet

1. Abre `snippets/octave.json`
2. Añade tu snippet siguiendo el formato estándar:

```json
"Octave Mi Snippet": {
    "prefix": "prefijo",
    "body": [
        "primera linea ${1:placeholder}",
        "\t${2:% cuerpo}",
        "end_keyword"
    ],
    "description": "Descripcion breve en español"
}
```

3. Verifica que el JSON sea válido: `python3 -m json.tool snippets/octave.json`
4. Abre un Pull Request

---

## Estándares de formato

### Sintaxis obligatoria (Octave 8.4.0)

| Usar | No usar |
|------|---------|
| `endfor` | `end` después de `for` |
| `endwhile` | `end` después de `while` |
| `endif` | `end` después de `if` |
| `endswitch` | `end` después de `switch` |
| `endfunction` | `end` después de `function` |
| `end_try_catch` | `end` después de `try` |
| `%` para comentarios | `#` (funciona pero no es idiomático) |

### Indentación

- Usar `\t` (tab) en el JSON para indentación dentro de bloques
- No usar espacios como indentación en snippets

### Comentarios en snippets

**Permitidos** — placeholders útiles que el usuario reemplaza:
```
% cuerpo del bucle
% rama verdadera
% tus variables aqui
```

**Prohibidos** — decoraciones o metadata:
```
%% ================
%% Autor: ...
%% ====== Fin ====
```

### Tab stops

- `${1:placeholder}` — primer tab stop con texto de ayuda
- `${2}` — tab stop vacío (cursor sin texto)
- Reutilizar el mismo número para texto que debe repetirse: `${1:retval}`
- Numerar en orden de flujo natural de escritura

---

## Convención de nombres para prefixes

| Categoría | Patrón | Ejemplos |
|-----------|--------|---------|
| Bucles | nombre del keyword | `for`, `while`, `do` |
| Variantes | sufijo de una letra | `fors` (step), `forn` (nested) |
| If/else | sufijo `e` por rama | `if`, `ife`, `ifee` |
| Funciones | `fun` + sufijo | `fun`, `funm`, `funv` |
| Matrices | `mat` + sufijo | `mat`, `matz`, `mato`, `mati` |
| Vectores | `vec` + sufijo | `vec`, `vecc`, `lsp` |
| Gráficos | `plot` + sufijo | `plot`, `plots`, `fig` |
| Printf | `pf` + sufijo | `pf`, `pfm` |

Regla general: **corto e intuitivo**. Si escribir el prefijo es más largo que escribir el código a mano, el prefijo es muy largo.

---

## Pull Request

El título debe seguir el formato:

```
[add] snippet `prefijo` para descripcion
[fix] snippet `prefijo` — descripcion del problema
[docs] actualizar README / CONTRIBUTING
```

Incluye en la descripción del PR:
- El snippet antes y después (si es una corrección)
- La fuente de la sintaxis (enlace a docs.octave.org si aplica)
- Versión de Octave probada

---

## Reportar un error

Usa [Issues](../../issues) e incluye:
- El prefix del snippet con problema
- El código generado (incorrecto)
- El código esperado (correcto)
- Tu versión de Octave: `octave --version`
