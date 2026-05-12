# Taller-práctico-04 Desafío de Consultor a Gobernanza Digital.
## López_Marco, Salas_Chema y Delgado_Pablo.

## Empresa
### Aceites del Aljarafe S.L.
#### Actualmente utilizan:
Excel para inventario.
Access para clientes.
Facturación manual.
Esto provoca errores, duplicidad de datos y poca eficiencia.

### ERP Elegido: SAP S/4HANA
Hemos elegido SAP por estos motivos:
Integración total de ventas, almacén, clientes y facturación.
Alta seguridad y control de permisos.
Gran capacidad de personalización para etiquetas y logística.
Escalabilidad para crecer en el futuro.
Soporte empresarial profesional.
Aunque es más caro que Odoo o Zoho One, es más robusto y preparado para empresas que quieren profesionalizarse.

# Seguridad RBAC

## Roles.

### Administrador
- Acceso total.

### Comercial
- Solo puede ver sus clientes y presupuestos.
- No puede ver stock ni contabilidad.

### Operario de almacén
- Solo puede gestionar stock y albaranes.

### Contable
- Puede gestionar facturas.
- No puede modificar inventario.

## Principio aplicado
**Mínimo privilegio:** cada usuario solo accede a lo necesario.

## Bloque B: Diseño de Seguridad RBAC (CE f)
El modelo de Control de Acceso Basado en Roles (RBAC) para SAP S/4HANA se ha diseñado bajo el Principio de Mínimo Privilegio. Esto garantiza que cada perfil cuente exclusivamente con las autorizaciones necesarias para desempeñar sus funciones, reduciendo riesgos de seguridad y errores operativos.

### Descripción de Roles
Administrador (Superusuario): Gestiona la totalidad del sistema. Posee acceso irrestricto a todos los módulos, configuraciones globales y gestión de usuarios. Es el responsable de supervisar que la integridad del ERP se mantenga intacta.

Comercial (Acceso Segmentado): Su alcance está limitado por reglas de registro (Record Rules). Solo puede visualizar y gestionar los clientes y presupuestos que tiene asignados, evitando la exposición de carteras ajenas y protegiendo la estrategia comercial.

Operario de Almacén (Gestión Logística): Su perfil es estrictamente operativo. Tiene permisos para consultar niveles de stock y gestionar albaranes de entrada y salida. No tiene visibilidad sobre márgenes de venta ni información contable sensible.

Contable (Control Financiero): Posee permisos de escritura y lectura en el módulo de facturación. Sin embargo, para mantener la segregación de funciones, tiene restringida la modificación de stock, asegurando que los registros financieros no alteren el inventario físico sin validación logística.
