# Compartiendo SQL con Git
Proyecto Grupal para Tecnicatura en Desarrollo de Software

# Objetivo
Compartir diferentes interpretaciones de sql para el siguiente caso:
- Mostrar en pantalla todos los Productos vendidos de la Sucursal  DE UN SUPERMERCADO del día de hoy.

# Interpretación 1:
```
SELECT p.*
FROM venta v
LEFT JOIN producto p ON d.rela_producto = p.id_producto
LEFT JOIN sucursal s ON p.rela_sucursal = s.id_sucursal
WHERE s.sucursal_descri = 'SUCURSAL A'
AND DATE(v.venta_fecha) >= DATE(NOW())
```