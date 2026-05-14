# Sistema de Gestión de Librería Nacional

Sistema robusto de inventario y ventas para librerías desarrollado en Python. Gestiona inventario de libros, registra ventas con descuentos por tipo de cliente, y genera reportes analíticos detallados.

---

## Características Principales

### Gestión de Inventario
- Agregar nuevos libros con información completa (título, autor, categoría, precio, stock)
- Actualizar información de libros existentes
- Eliminar libros del inventario
- Visualizar inventario completo con detalles

### Sistema de Ventas
- Registro de ventas con validación de stock
- Sistema de descuentos por tipo de cliente:
  - **Regular**: 0% descuento
  - **VIP**: 10% descuento
  - **Mayorista**: 15% descuento
- Generación automática de recibos
- Historial completo de ventas con totales

### Reportes y Análisis
- Top 3 libros más vendidos
- Ventas agrupadas por autor
- Análisis de rendimiento de inventario
- Cálculo de ingresos totales y valor de inventario

### Persistencia de Datos
- Guardado automático en formato JSON
- Carga de datos al iniciar el sistema
- Manejo robusto de errores y datos corruptos

---

## Requisitos del Sistema

- **Python**: 3.7 o superior
- **Sistema Operativo**: Windows, macOS, Linux
- **Librerías estándar**: `json`, `os`, `datetime` (incluidas en Python)

**No requiere instalación de dependencias externas** ✨

---

## Instalación

### 1. Clonar o descargar el proyecto

```bash
git clone https://github.com/tu-usuario/sistema-libreria.git
cd sistema-libreria
```

### 2. Verificar estructura de carpetas

```
sistema-libreria/
│
├── main.py                          # Archivo principal
├── Details.py                       # Configuración y variables globales
│
├── Functions/
│   ├── Functions_Files.py          # Gestión de archivos JSON
│   ├── Functions_Inventory.py      # CRUD de inventario
│   ├── Functions_Sale.py           # Gestión de ventas
│   └── Functions_Report.py         # Generación de reportes
│
└── Datos/                           # Carpeta de datos (se crea automáticamente)
    ├── inventory.json               # Inventario persistente
    └── sales.json                   # Historial de ventas
```

### 3. Ejecutar el programa

```bash
python main.py
```

---

## Uso del Sistema

### Menú Principal

Al iniciar el programa, verás el siguiente menú:

```
==================================================
NATIONAL BOOKSTORE DIGITAL AREA - ROBUST SYSTEM
==================================================
1. Show all books
2. Add new book
3. Update book
4. Delete book
5. Record sale
6. Show sales history
7. Top 3 best-selling books
8. Sales by brand
9. Inventory performance
0. Exit
==================================================
```
---

## Estructuras de Datos

### Inventario (Dictionary)
```python
{
    "P001": {
        "title": "Don Quijote de la Mancha",
        "author": "Miguel de Cervantes",
        "category": "Novela",
        "price": 89560,
        "stock": 10
    }
}
```

### Ventas (List of Dictionaries)
```python
[
    {
        "customer": "María González",
        "customer_type": "vip",
        "code_product": "P002",
        "name_book": "Cien años de soledad",
        "author": "Gabriel García Márquez",
        "quantity": 3,
        "price_unitario": 6000,
        "discount_percentage": 10,
        "total": 16200.0,
        "date": "2024-11-25 14:30:45"
    }
]
```

### Descuentos (Dictionary)
```python
{
    "regular": 0,
    "vip": 10,
    "wholesaler": 15
}
```

---

## Tecnologías Utilizadas

| Tecnología | Uso |
|------------|-----|
| **Python 3.x** | Lenguaje principal |
| **JSON** | Formato de almacenamiento |
| **datetime** | Registro de timestamps |
| **os** | Gestión de archivos y directorios |

---
