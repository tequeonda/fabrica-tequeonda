# 🎨 Ficha de Tema Visual — Teque Onda

> Pegá este archivo (o su contenido) al inicio de cualquier chat y pedí:
> **"Aplicá el tema visual Teque Onda a este artefacto"**

---

## Concepto
Tema **claro** (fondo blanco), profesional, con la identidad de la fábrica.
Jerarquía de color: **Dorado dominante (marca y acción) · Negro estructural (headers, KPIs) · Verde de acento (totales, confirmaciones).**
Tipografía display (Bebas Neue) para títulos y números, Oswald para códigos de producto, Fira Sans para cuerpo.

---

## Paleta de colores

| Rol | Hex | Uso |
|-----|-----|-----|
| Amarillo dorado | `#FFC72C` | **Color dominante**: cabeceras de categoría, botón principal, pestañas activas, líneas de header, badges de total |
| Negro (ink) | `#111111` | **Estructura**: barra de modos, KPIs, header de freezer, texto sobre dorado |
| Verde institucional | `#00a82d` | **Acento**: totales de producto, valores de tendencia, números de carga |
| Verde brillante | `#00d838` | Números de total sobre negro, fecha en header |
| Dorado oscuro | `#c79500` | Texto dorado sobre fondo claro |
| Fondo página | `#f4f3ee` | Background general |
| Card / superficie | `#ffffff` | Paneles, tarjetas |
| Línea / borde | `#e6e4db` | Separadores, bordes de cards |
| Texto principal | `#222222` | Cuerpo de texto |
| Texto apagado | `#888888` | Labels, hints, subtítulos |
| Rojo alerta | `#e23b3b` | Alertas críticas |
| Naranja alerta | `#e07c14` | Alertas medias |

## Colores por categoría de producto (barra lateral + fondo claro)

| Categoría | Color barra | Fondo claro |
|-----------|-------------|-------------|
| TEQUEÑOS | `#FFC72C` | `#fffdf5` |
| PASTELITOS | `#FF8A4C` | `#fffaf6` |
| MINI EMPANADAS | `#3fae6e` | `#f7fdf9` |
| POSTRES | `#9B6BE0` | `#faf7fe` |
| CACHITOS | `#E0A92C` | `#fdfaf2` |
| BEBIDAS | `#3499c7` | `#f4fbfe` |
| SALSAS | `#D85A85` | `#fef6f9` |

---

## Tipografía

Importar:
```html
<link href="https://fonts.googleapis.com/css2?family=Bebas+Neue&family=Fira+Sans:wght@400;500;600;700&family=Oswald:wght@500;600;700&display=swap" rel="stylesheet">
```

- **Bebas Neue** → títulos, encabezados de sección, números grandes, marca. Siempre con `letter-spacing` 2-3px.
- **Fira Sans** → cuerpo de texto, nombres de producto, párrafos.
- **Oswald** (weight 600) → códigos de producto (TO, TF, EQ...), dentro de un badge crema.

Tamaños base: cuerpo 15px, títulos de sección 15px, números KPI 36px, números de stock 17-18px.

---

## Componentes clave

### Header de marca (negro con línea dorada)
```html
<div style="background:#111;padding:12px 16px;display:flex;justify-content:space-between;align-items:center;border-bottom:4px solid #FFC72C;">
  <span style="font-family:'Bebas Neue';font-size:22px;color:#fff;letter-spacing:3px;">🧀 TEQUE <span style="color:#FFC72C;">ONDA</span></span>
  <span style="font-family:'Bebas Neue';font-size:14px;color:#FFC72C;letter-spacing:2px;">VIERNES</span>
</div>
```

### Badge de código (Oswald sobre crema)
```html
<span style="font-family:'Oswald';font-weight:600;font-size:13px;letter-spacing:1px;color:#111;background:#eceae3;padding:1px 7px;border-radius:5px;">TO</span>
```

### Bloque de categoría (barra lateral + cabecera dorada, texto negro)
```html
<div style="border-left:5px solid #FFC72C;background:#fffdf5;border-radius:0 9px 9px 0;border:1px solid #e6e4db;overflow:hidden;">
  <div style="background:#FFC72C;padding:5px 12px;font-family:'Bebas Neue';font-size:15px;letter-spacing:2px;color:#111;display:flex;justify-content:space-between;">
    <span>🧀 TEQUEÑOS</span><span style="color:#1a6b1a;">132</span>
  </div>
  <!-- filas de producto aquí. La cabecera usa el color de la categoría como fondo. -->
</div>
```

### KPI (negro con número dorado)
```html
<div style="background:#111;border-radius:11px;padding:14px 12px;">
  <div style="font-family:'Bebas Neue';font-size:36px;color:#FFC72C;line-height:1;">1.450</div>
  <div style="font-size:11px;color:#bbb;text-transform:uppercase;letter-spacing:.5px;margin-top:4px;">En stock total</div>
</div>
```

### Botón principal (dorado, texto negro)
```html
<button style="background:#FFC72C;color:#111;border:none;padding:14px;font-family:'Bebas Neue';font-size:21px;letter-spacing:2px;border-radius:9px;width:100%;">▶ GUARDAR</button>
```

### Pestañas (negro con activa dorada)
```html
<div style="display:flex;gap:4px;background:#111;border-radius:10px;padding:4px;">
  <button style="flex:1;padding:9px;font-family:'Bebas Neue';font-size:14px;letter-spacing:2px;color:#111;background:#FFC72C;border:none;border-radius:7px;">ACTIVA</button>
  <button style="flex:1;padding:9px;font-family:'Bebas Neue';font-size:14px;letter-spacing:2px;color:#999;background:none;border:none;border-radius:7px;">INACTIVA</button>
</div>
```

---

## Reglas de estilo
- Fondo siempre claro (`#f4f3ee` página, `#ffffff` tarjetas).
- **Dorado es el color dominante**: cabeceras de categoría (fondo dorado, texto negro), botón principal, pestañas activas, líneas de header, badges de total.
- **Negro es estructural**: barra de modos, KPIs (fondo negro, número dorado), header de freezer (fondo negro con línea dorada abajo). Da peso y evita que el dorado sature.
- **Verde es acento puntual**: totales de producto en tablas, valores de tendencia, mensaje de guardado, foco de inputs.
- Texto sobre dorado SIEMPRE negro `#111`. Totales sobre cabecera dorada en verde oscuro `#1a6b1a` para legibilidad.
- Títulos y números en Bebas Neue con buen interletrado.
- Códigos de producto SIEMPRE en Oswald sobre badge crema `#eceae3`.
- Categorías con barra lateral de 5px del color de categoría + cabecera negra.
- Interlineado compacto en listas de producto (padding vertical 2-3px por fila).
- Bordes sutiles `#e6e4db`, radios 8-13px.
- Para tablas de stock por freezer: columnas F1/F2/F3/Total, ceros en gris muy claro `#cfcfc8`.
