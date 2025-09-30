# Aplicación Demo con Tkinter

## 📖 Descripción General
Este proyecto es un **MVP (Minimum Viable Product)** desarrollado en **Python** utilizando la librería **Tkinter** para construir interfaces gráficas.

La aplicación presenta un menú principal desde donde se accede a cinco ventanas independientes:

1. **Home / Bienvenida**  
2. **Formulario (Entrada y validación de datos)**  
3. **Lista (CRUD básico)**  
4. **Tabla (Treeview con datos desde CSV)**  
5. **Canvas (Dibujo)**  

Cada ventana está modularizada en un archivo independiente, lo que facilita la **escalabilidad y mantenibilidad** del proyecto.

---

## 📂 Estructura de Archivos
```
proyecto/
│
├── main.py              # Ventana principal y punto de entrada
├── app/
│   ├── win_home.py      # Ventana de bienvenida
│   ├── win_form.py      # Ventana con formulario
│   ├── win_list.py      # Ventana CRUD con Listbox
│   ├── win_table.py     # Ventana con Treeview y carga CSV
│   ├── win_canvas.py    # Ventana con dibujo Canvas
│
└── data/
    └── sample.csv       # Datos de ejemplo para win_table
```

---

## 📑 Descripción de Archivos

### 🔹 `main.py`
- Define la ventana principal (`Tk`).
- Contiene botones para abrir las 5 ventanas.
- Proporciona navegación centralizada.
- Usa `ttk.Frame` para organizar los botones.
- Cierra la aplicación con el botón **Salir**.

👉 Función principal: `main()`

---

### 🔹 `win_home.py`
- Muestra una ventana de bienvenida.
- Componentes principales:
  - Etiquetas con texto introductorio.
  - Botón que despliega un `messagebox` de información.
  - Botón para cerrar la ventana.

👉 Función: `open_win_home(parent)`

---

### 🔹 `win_form.py`
- Implementa un formulario con validación de datos:
  - **Nombre** (campo de texto obligatorio).
  - **Edad** (debe ser un número entero).
- Incluye funcionalidad para **guardar datos en un archivo `.txt`** usando `filedialog`.
- Retroalimentación con `messagebox` en caso de errores o éxito.

👉 Función: `open_win_form(parent)`

---

### 🔹 `win_list.py`
- Implementa un CRUD básico con un **Listbox**:
  - **Agregar** elementos desde un `Entry`.
  - **Eliminar** elemento seleccionado.
  - **Limpiar** lista completa.
- Usa un `grid` para disposición flexible.

👉 Función: `open_win_list(parent)`

---

### 🔹 `win_table.py`
- Presenta datos tabulares en un **Treeview**.
- Columnas: `nombre`, `valor1`, `valor2`.
- Carga datos desde el archivo **`data/sample.csv`**.
- Si el archivo no existe, muestra advertencia.

👉 Función: `open_win_table(parent)`

---

### 🔹 `sample.csv`
Archivo de datos de ejemplo en formato CSV:

```csv
nombre,valor1,valor2
A,10,20
B,15,25
C,12,30
```

---

### 🔹 `win_canvas.py`
- Demostración del widget **Canvas**:
  - Rectángulo, óvalo, línea y texto.
- Muestra cómo dibujar elementos gráficos personalizados.

👉 Función: `open_win_canvas(parent)`

---

## ⚙️ Tecnologías Utilizadas
- **Python 3.x**
- **Tkinter** (interfaz gráfica estándar en Python)
- **ttk** (temas y widgets mejorados)
- **csv**, **pathlib**, **filedialog**, **messagebox** (utilidades estándar)

---

## 🚀 Potenciales Mejoras
1. Persistencia en **Base de Datos** (SQLite) para CRUD.
2. Diseño modular para **tests unitarios**.
3. Estilo unificado mediante **ttk.Style**.
4. Internacionalización (i18n) para múltiples idiomas.
5. Integración de **imágenes y gráficos** en Canvas y tablas.

---

## ▶️ Ejecución
```bash
python main.py
```
