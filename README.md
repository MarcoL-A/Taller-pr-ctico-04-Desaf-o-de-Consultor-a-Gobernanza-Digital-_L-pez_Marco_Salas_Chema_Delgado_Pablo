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

## Roles

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
