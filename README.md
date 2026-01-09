# Tapiz — Observador Estructural Mínimo

Tapiz es un producto matemático mínimo para **observar estructura**, no datos.

No predice.  
No optimiza.  
No aprende pesos.

Solo **mide estabilidad y cambio estructural** a partir de relaciones espectrales simples.

---

## Idea central

> **El Tapiz no memoriza datos.  
> Memoriza cambios estructurales.**

Dos señales distintas pueden compartir el mismo Tapiz  
si su estructura es equivalente.

---

## Qué hace Tapiz

- Observa una ventana de datos numéricos
- Extrae una relación espectral mínima (`lambda2_norm`)
- Clasifica el estado en un **régimen estructural**
- Recuerda **solo cuando algo cambia de verdad**

---

## Qué NO hace

- ❌ No predice el futuro  
- ❌ No clasifica con Machine Learning  
- ❌ No entrena modelos  
- ❌ No depende de un dominio específico  

Tapiz es **agnóstico al significado de los datos**.

---

## Componentes

- `state.py`  
  Define el estado Tapiz (inmutable).

- `core.py`  
  Realiza la observación estructural.

- `memory.py`  
  Memoria selectiva: guarda solo eventos relevantes.

- `main.py`  
  Ejecución de ejemplo.

---

## Ejemplo mínimo

```python
state = observe_window(X)
event = memory.observe(state)

print(state)