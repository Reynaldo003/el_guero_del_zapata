# El Güero del Zapata — Demo de administración

Demo de interfaz para administración y operación del restaurante, desarrollada con **React 18 + Vite + Tailwind CSS + Lucide + Recharts**.

## Instalación

1. Instala Node.js 20 o superior.
2. Abre una terminal dentro de esta carpeta.
3. Ejecuta `npm install`.
4. Ejecuta `npm run dev`.
5. Abre la URL local indicada por Vite (normalmente http://localhost:5173).

Para compilar: `npm run build`. Los archivos finales quedan en `dist/`.

Si PowerShell impide ejecutar npm por la política de scripts en Windows, abre **Símbolo del sistema (CMD)** y ejecuta ahí `npm install` y `npm run dev`, o utiliza `npm.cmd install` y `npm.cmd run dev` desde PowerShell. No es necesario modificar la política de seguridad del equipo.

## Funcionalidad disponible

- Dashboard administrativo con indicadores y gráficas ilustrativas.
- Mapa de 16 mesas y registro de número de personas / mesera.
- Captura de comandas para mesa, mostrador y mensaje.
- Distribución **automática por producto** a las estaciones Taqueros, Picaditas, Consomés y Bebidas.
- Cuatro vistas de cocina que permiten pasar cada partida de pendiente → preparando → listo.
- Pedidos para llevar y por mensaje con nombre, teléfono y dirección.
- Cobros de demostración por efectivo, tarjeta o transferencia, cierre de cuentas e historial.
- Catálogo editable de productos con precio, estación asignada y disponibilidad.
- Inventario de materias primas con entradas/salidas manuales y mínimos.
- Reportes, exportación CSV de los pagos registrados y lista de colaboradores.
- Diseño responsive para tablets y computadoras, con menú móvil.
- Persistencia de cambios en `localStorage` del navegador y opción para reiniciar la demo.

## Limitaciones importantes

**Es una demo frontend, no un sistema productivo**. No hay backend, base de datos compartida, autenticación, roles, impresoras, procesamiento bancario, WhatsApp conectado, pedidos externos en tiempo real, sincronización entre diferentes tablets ni descuentos por receta. El estado se guarda únicamente en el navegador del dispositivo que lo utiliza. Las ventas históricas iniciales, clientes y estadísticas son datos ilustrativos, no información real del negocio. El catálogo y precios también son ejemplos que deben validarse con el restaurante.

Para una implementación operativa se recomienda crear un backend con base de datos y eventos en tiempo real (por ejemplo Spring Boot o Node.js + PostgreSQL + WebSocket), control de permisos, cortes de caja auditables, recetas y movimientos de inventario transaccionales, control de sucursales, respaldos y despliegue seguro.

## Archivos importantes

- `src/App.jsx`: pantallas, navegación y lógica de demostración.
- `src/styles.css`: Tailwind y estilos del diseño.
- `public/assets/`: recursos gráficos basados en la identidad e imágenes de referencia.

La demo está preparada para sustituir la lógica de `localStorage` por llamadas a una API en una siguiente etapa.
