# Simulacro II de consultas SQL

## Bases de Datos
### Marc Morlá Isern
### 02/06/2023


1. SELECT titulo FROM libros INNER JOIN prestamos ON libros.id_libro = prestamos.id_libro WHERE id_prestamo='1';

2. SELECT DISTINCT id_libro, titulo FROM libros INNER JOIN prestamos ON libros.id_libro = prestamos.id_libro WHERE prestamo.fecha_prestamo < DATE_SUB(CURDATE(), INTERVAL 6 MONTH)

3. SELECT MAX(fecha_prestamo) FROM prestamos GROUP BY 'year'

4. SELECT AVG(autor) FROM libros LEFT JOIN ON libros.id_libro = prestamos.id_libro WHERE id_prestamo < 3

5. SELECT * FROM prestamos WHERE fecha_devolucion IS NULL

6. SELECT titulo FROM libros INNER JOIN prestamos ON libros.id_libro = prestamos.id_libro WHERE prestamos.fecha_prestamo >= DATE_SUB(CURDATE(), INTERVAL 1 MONTH)

7. SELECT DISTINCT MAX(autor) FROM libros

8. SELECT titulo FROM libros LEFT JOIN prestamos ON libros.id_libro = prestamos.id_libro WHERE MAX(titulo) GROUP BY ASC

9. SELECT titulo FROM libros LEFT JOIN prestamos ON libros.id_libro = prestamos.id_libro WHERE prestamos.id_libro IS NULL

10. 
