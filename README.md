# Demo de demostración

Esta versión fue preparada exclusivamente para mostrar las funcionalidades de la aplicación.

- Funciona localmente y no requiere conexión a una base de datos externa.
- Utiliza datos ficticios para simular operaciones reales.
- Permite explorar las funcionalidades sin acceder a información de producción.
- Los datos se almacenan localmente en el entorno de ejecución.

Nota: Esta versión es independiente del entorno de producción y no tiene acceso a sus bases de datos ni credenciales.




# Leyra Seguridad

Aplicación local organizada por pantallas y módulos para gestionar los servicios de Leyra Seguridad.

## Inicio

Abrir `dashboard.html` en el navegador o ejecutar la aplicación de escritorio con Electron:

1. Instalar Node.js (versión LTS).
2. Desde esta carpeta, ejecutar `npm install` en CMD o `npm.cmd install` en PowerShell.
3. Iniciar la aplicación con `npm start` en CMD o `npm.cmd start` en PowerShell.

Electron abre `dashboard.html` como ventana nativa. Los datos se guardan en el almacenamiento local de esa instalación de la aplicación.

## Pantallas

- `dashboard.html`: inicio y resumen de órdenes.
- `clientes.html`: directorio de clientes.
- `ordenes.html`: órdenes de servicio.
- `presupuestos.html`: cotizador e historial de presupuestos.
- `equipos.html`: equipos y objetos vinculados a clientes.
- `inventario.html`: materiales y stock.

En presupuestos se puede imprimir una propuesta de insumos sin mano de obra o una factura final que incluye la mano de obra como un solo total. El cálculo interno de la mano de obra usa horas y valor por hora. Se pueden configurar el nombre comercial, frase, contactos, logo, color y estilo del documento desde «Marca y estética del presupuesto»; la identidad visual queda guardada localmente. También se pueden agregar servicios ofrecidos desde el selector del cotizador; quedan guardados en el navegador para futuros presupuestos. Las categorías de inventario se pueden ampliar desde el formulario para agregar materiales. Las órdenes no requieren asignar un técnico.

## Recursos compartidos

- `js/core.js`: datos compartidos, almacenamiento local, navegación y utilidades.
- `js/dashboard.js`, `js/clients.js`, `js/orders.js`, `js/quotes.js`, `js/objects.js`, `js/inventory.js`: lógica de cada módulo.
- `css/app.css`: estilos compartidos y plantilla de impresión.

Los registros continúan guardándose en el almacenamiento local del navegador.
