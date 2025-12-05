# Microservicio de Productos - NestJS

Este proyecto es un **microservicio NestJS** que provee los productos de ahorro digital mediante **API REST**, reemplazando los JSON locales utilizados anteriormente en el frontend.  

---

## 🏗 Estructura del proyecto

/backend
/src
/products
products.module.ts
products.service.ts
products.controller.ts
main.ts
app.module.ts

- **ProductsService**: contiene la data de productos y métodos para filtrarlos.  
- **ProductsController**: expone los endpoints REST `/products` y `/products/search`.  

---

## ⚡ Requisitos

- Node.js >= 18
- npm o yarn

---

## 🚀 Levantar el microservicio

### 1. Instalar dependencias

```bash
npm install

npm run start:dev
```
	Por defecto corre en: http://localhost:3000
	•	Si quieres cambiar el puerto, modifica main.ts:

await app.listen(4000);

🔧 Notas técnicas

	•	Este microservicio es independiente y puede ser consumido por cualquier frontend mediante REST.
	•	Está listo para ser escalable y desplegado de manera independiente.
	•	Puede reemplazar los JSON locales del frontend, centralizando la data de productos.

  ✅ Cómo probar
  
	1.	Levanta el microservicio: npm run start:dev.
	2.	Abre un navegador o Postman y accede a los endpoints (/products o /products/search?q=...).
	3.	Integra con el frontend Next.js apuntando a http://localhost:3000/products.