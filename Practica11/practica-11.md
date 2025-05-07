# Modelado de Datos - TechGadget

## Modelo Entidad-Relación

### Entidades Principales:
1. **Usuario**
   - id_usuario (PK)
   - nombre
   - email
   - dirección
   - teléfono

2. **Producto**
   - id_producto (PK)
   - nombre
   - descripción
   - precio
   - stock
   - id_categoria (FK)

3. **Categoría**
   - id_categoria (PK)
   - nombre
   - descripción

4. **Orden**
   - id_orden (PK)
   - id_usuario (FK)
   - fecha
   - total
   - estado

5. **DetalleOrden**
   - id_detalle (PK)
   - id_orden (FK)
   - id_producto (FK)
   - cantidad
   - precio_unitario

### Relaciones:
- Usuario genera Orden (1:N)
- Orden contiene DetalleOrden (1:N)
- Producto pertenece a Categoría (N:1)
- DetalleOrden referencia Producto (N:1)

## Diagrama Relacional
![Diagrama Relacional TechGadget](/Practica11/assets/diagrama-relacional-techgadget.png)

## Implementación en Supabase

He implementado el modelo de datos en Supabase siguiendo estos pasos:

1. Creé un nuevo proyecto en Supabase llamado "techgadget-db"
2. Configuré las tablas según el modelo relacional:
   - `usuarios`
   - `productos`
   - `categorias`
   - `ordenes`
   - `detalle_ordenes`
3. Establecí las relaciones entre las tablas usando claves foráneas
4. Configuré los tipos de datos apropiados para cada campo

### Captura del Schema Visualizer de Supabase

![Modelo de datos en Supabase](/Practica11/assets/supabase-schema-techgadget.png)
