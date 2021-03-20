# 05-NombreyGridGridTemplateArea
* Grid Layout creado con nombres y grid. grid-template-areas y usando grid

```javascript
/* Usando grid-template-areas */
.contenedor1 {
    height: 100vh;
    width: 900px;
    margin: 0 auto;
    display: grid;
    /* grid: row / column */
    /* en row 100 arriba auto en medio 100 abajo.  */
    /* en column son 4 calumnas de 25% */
    grid: 100px auto 100px / repeat(4, 25%);
    grid-template-areas: 
    /* No contar lineas. Contar los elementos */
    /* puede ser cualquier nombre. */
    /* agregar un nombre por cada columna que se requira */
    /* el nombre debe ser igual en el elemento hijo usando grid-area */
        "header header header header"
        "principal principal principal sidebar"
/* el punto quita la primera caja. el contenido se mueve a la segunda caja */
        ". footer footer footer";
/* gap  para dar margen a cada seccion*/
/* agranda el sitio por culpa del margen */
/* row-gap y column-gap */
gap: 1rem;
}

.header1 {
    background-color: coral;
    color: white;
    text-align: center;
    /* debe ser el mismo nombre que se usa en grid-template-areas: header; */
    grid-area: header;
   
}

.contenido-principal1 {
    background-color: darkred;
    grid-area: principal;
   
}
.sidebar1 {
    background-color: olive;
   
}
.footer1 {
    background-color: navy;
    grid-area: footer;
   
}
```
