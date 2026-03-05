# Unidad 2: Diseño y modelado de microservicios

## 🎯 Objetivos de aprendizaje

Al finalizar esta unidad, el estudiante será capaz de:

1. **Aplicar** domain-driven design (DDD) para definir bounded contexts
2. **Diseñar** APIs RESTful siguiendo principios de madurez y especificarlas con OpenAPI
3. **Identificar** y aplicar patrones arquitectónicos: API Gateway, Saga, CQRS, Event Sourcing
4. **Modelar** la comunicación entre microservicios usando context mapping
5. **Preparar** el diseño base para la plataforma de ingesta y procesamiento de datos

---

## 📚 Estructura del contenido

```text
unidad-2-diseno/
├── 01-teoria/        # Conceptos de DDD, APIs y patrones
├── 02-recursos/      # Material complementario y herramientas
└── 03-actividades/   # Ejercicios de modelado y análisis
```

### 📖 [Teoría](01-teoria/README.md)

Conceptos fundamentales organizados en tres módulos principales:

#### 2.1 Domain-driven design (DDD) y contextos

- **Conceptos centrales:** Dominio, Modelo, Lenguaje Ubicuo
- **Bounded Contexts:** Delimitación de responsabilidades
- **Context Mapping:** Patrones de colaboración entre contextos

#### 2.2 Diseño de APIs y contratos

- **Richardson Maturity Model:** Niveles 0-3 de madurez RESTful
- **OpenAPI/Swagger:** Especificación completa de contratos de API
- **Versionado y documentación:** Estrategias de evolución de APIs

#### 2.3 Patrones arquitectónicos de integración

- **API Gateway:** Punto de entrada único y funcionalidades transversales
- **Saga Pattern:** Transacciones distribuidas con compensación
- **CQRS y Event Sourcing:** Separación de responsabilidades y auditabilidad

---

## 🔗 Conexión con el proyecto final


Esta unidad establece el **diseño arquitectónico base** para el proyecto final:

### Bounded contexts del proyecto

Aplicando DDD al **"Sistema de E-commerce basado en microservicios"**:

1. **Catálogo Context** - Gestión de productos y categorías
   - Entidades: Product, Category, Inventory
   - APIs: Product Catalog API

2. **Clientes Context** - Registro y gestión de clientes
   - Entidades: Customer, Address, Profile
   - APIs: Customer Management API

3. **Pedidos Context** - Creación y seguimiento de pedidos
   - Entidades: Order, OrderItem, Payment
   - APIs: Order Management API

4. **Carrito Context** - Operaciones sobre el carrito de compras
   - Entidades: Cart, CartItem
   - APIs: Shopping Cart API

5. **Pagos y Fulfillment Context** - Procesamiento de pagos y envíos
   - Entidades: Payment, Shipment, Tracking
   - APIs: Payment API, Fulfillment API

### Patrones arquitectónicos aplicables

- **API Gateway:** Punto de entrada único para todas las APIs del sistema
- **Saga Pattern:** Coordinación de pedidos multi-etapa
- **CQRS:** Separación de APIs de escritura (pedidos) vs consulta (historial)
- **Event Sourcing:** Auditabilidad de operaciones de pedidos y pagos

---

**Anterior:** [← Unidad 1: Introducción](../unidad-1-introduccion/README.md) | **Siguiente:** [Unidad 3: Implementación →](../unidad-3-implementacion/README.md)

---

*Esta unidad transforma los conceptos fundamentales de la Unidad 1 en diseños arquitectónicos concretos, preparando la implementación práctica que comenzará en la Unidad 3.*
