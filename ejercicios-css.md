# Ejercicios Prácticos de CSS

## 🎯 Objetivo
Estos ejercicios están diseñados para que los diseñadores gráficos practiquen y refuercen los conceptos de CSS utilizando esta plantilla de blog como base.

## 📋 Instrucciones Generales
1. Haz una copia de los archivos originales antes de comenzar
2. Modifica solo los archivos CSS e HTML según se indique
3. Prueba tus cambios en el navegador después de cada ejercicio
4. Experimenta con diferentes valores para entender mejor cada propiedad

---

## Ejercicio 1: Personalización de Colores
**Dificultad:** ⭐ Principiante

### Objetivo
Crear un esquema de colores personalizado usando CSS Custom Properties (variables).

### Tareas
1. **Añadir variables CSS** al inicio del archivo `styles.css`:
```css
:root {
  --color-primary: #your-color;
  --color-secondary: #your-color;
  --color-accent: #your-color;
  --color-text: #your-color;
  --color-background: #your-color;
}
```

2. **Reemplazar colores hardcodeados** con las variables:
   - Cambia `#000` por `var(--color-primary)`
   - Cambia `#fafafa` por `var(--color-background)`
   - Cambia `#1a1a1a` por `var(--color-text)`

3. **Crear tres variaciones** de color:
   - Tema claro (colores suaves)
   - Tema oscuro (colores oscuros)
   - Tema vibrante (colores llamativos)

### Bonus
- Añade un botón para cambiar entre temas usando JavaScript

---

## Ejercicio 2: Modificación del Layout Grid
**Dificultad:** ⭐⭐ Intermedio

### Objetivo
Experimentar con diferentes configuraciones de CSS Grid.

### Tareas
1. **Cambiar el grid principal** (`.content-grid`):
   - Prueba: `grid-template-columns: 2fr 1fr`
   - Prueba: `grid-template-columns: 300px 1fr`
   - Prueba: `grid-template-columns: 1fr` (sin sidebar)

2. **Modificar el grid de artículos** (`.main-articles`):
   - Cambiar a 3 columnas fijas: `grid-template-columns: repeat(3, 1fr)`
   - Usar diferentes tamaños mínimos: `minmax(200px, 1fr)`
   - Experimentar con `grid-auto-flow: dense`

3. **Crear un layout alternativo**:
   - Sidebar arriba del contenido en móviles
   - Grid de artículos en una sola columna en tablets

### Bonus
- Añade `grid-template-areas` para nombrar las áreas del layout

---

## Ejercicio 3: Tipografía y Escalas
**Dificultad:** ⭐⭐ Intermedio

### Objetivo
Implementar un sistema tipográfico coherente.

### Tareas
1. **Crear una escala tipográfica** usando variables:
```css
:root {
  --font-size-xs: 0.75rem;
  --font-size-sm: 0.875rem;
  --font-size-base: 1rem;
  --font-size-lg: 1.125rem;
  --font-size-xl: 1.25rem;
  --font-size-2xl: 1.5rem;
  --font-size-3xl: 1.875rem;
  --font-size-4xl: 2.25rem;
}
```

2. **Aplicar la escala** a todos los elementos de texto
3. **Experimentar con diferentes font-families**:
   - Serif para títulos
   - Sans-serif para cuerpo
   - Monospace para código

4. **Añadir font-weights** apropiados:
   - 300 (light), 400 (regular), 500 (medium), 600 (semibold), 700 (bold)

### Bonus
- Implementa `clamp()` para tipografía fluida

---

## Ejercicio 4: Animaciones y Transiciones
**Dificultad:** ⭐⭐⭐ Avanzado

### Objetivo
Añadir animaciones suaves y atractivas.

### Tareas
1. **Mejorar las transiciones existentes**:
   - Añadir `transition` a más elementos
   - Experimentar con diferentes `timing-functions`
   - Usar `transform` en lugar de cambiar propiedades que causan reflow

2. **Crear animaciones de entrada**:
```css
@keyframes fadeInUp {
  from {
    opacity: 0;
    transform: translateY(30px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
```

3. **Añadir hover effects avanzados**:
   - Escalado suave en cards
   - Cambios de color graduales
   - Efectos de sombra

### Bonus
- Implementa animaciones con `scroll-triggered` usando CSS o JavaScript

---

## Ejercicio 5: Responsive Design Avanzado
**Dificultad:** ⭐⭐⭐ Avanzado

### Objetivo
Optimizar la experiencia en todos los dispositivos.

### Tareas
1. **Añadir más breakpoints**:
```css
/* Mobile first approach */
@media (min-width: 480px) { /* Small mobile */ }
@media (min-width: 768px) { /* Tablet */ }
@media (min-width: 1024px) { /* Desktop */ }
@media (min-width: 1200px) { /* Large desktop */ }
```

2. **Optimizar la navegación móvil**:
   - Crear un menú hamburguesa
   - Implementar navegación off-canvas

3. **Usar Container Queries** (si el navegador lo soporta):
```css
@container (min-width: 400px) {
  .article-card {
    /* Estilos cuando el contenedor es >= 400px */
  }
}
```

### Bonus
- Implementa `prefers-reduced-motion` para accesibilidad

---

## Ejercicio 6: Componentes Modulares
**Dificultad:** ⭐⭐⭐ Avanzado

### Objetivo
Crear un sistema de componentes reutilizables.

### Tareas
1. **Crear clases de utilidad**:
```css
/* Spacing utilities */
.mt-1 { margin-top: 0.25rem; }
.mt-2 { margin-top: 0.5rem; }
/* ... más utilidades */

/* Color utilities */
.text-primary { color: var(--color-primary); }
.bg-primary { background-color: var(--color-primary); }
```

2. **Modularizar componentes**:
   - Separar estilos de botones
   - Crear variantes de cards
   - Sistematizar formularios

3. **Implementar BEM methodology**:
```css
.card { /* Block */ }
.card__header { /* Element */ }
.card--featured { /* Modifier */ }
```

### Bonus
- Organiza el CSS en múltiples archivos usando `@import`

---

## 🎨 Proyectos Finales

### Proyecto A: Rediseño Completo
- Cambia completamente el diseño visual manteniendo la estructura HTML
- Implementa un tema único (ej: estilo magazine, minimalista, colorido)
- Añade nuevas secciones o componentes

### Proyecto B: Blog Temático
- Adapta el contenido a un tema específico (fotografía, cocina, tecnología)
- Personaliza colores, tipografías y layouts según el tema
- Añade elementos visuales apropiados

### Proyecto C: Versión Dark Mode
- Implementa un sistema completo de tema oscuro
- Añade toggle para cambiar entre temas
- Considera la accesibilidad y contraste

---

## 📚 Recursos Adicionales

- [MDN CSS Reference](https://developer.mozilla.org/en-US/docs/Web/CSS)
- [CSS Grid Guide](https://css-tricks.com/snippets/css/complete-guide-grid/)
- [Flexbox Guide](https://css-tricks.com/snippets/css/a-guide-to-flexbox/)
- [CSS Custom Properties](https://developer.mozilla.org/en-US/docs/Web/CSS/--*)
- [Can I Use](https://caniuse.com/) - Compatibilidad de navegadores

## 💡 Consejos

1. **Experimenta sin miedo**: CSS es muy visual, prueba diferentes valores
2. **Usa las herramientas de desarrollador**: Inspecciona y modifica en tiempo real
3. **Comenta tu código**: Explica por qué hiciste ciertos cambios
4. **Valida tu CSS**: Usa herramientas online para verificar errores
5. **Piensa en la accesibilidad**: Considera usuarios con diferentes necesidades

¡Diviértete aprendiendo CSS! 🚀