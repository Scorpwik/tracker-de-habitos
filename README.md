# Mis hábitos

Tablero web para anotar los hábitos del día, marcarlos cuando ya se cumplieron y ver cuántos faltan. Todo se guarda en el navegador: no hay cuentas ni servidor propio.

**Demo:** [scorpwik.github.io/tracker-de-habitos](https://scorpwik.github.io/tracker-de-habitos/)

## Qué hace

- Agregar un hábito desde el formulario. Si el texto queda vacío, no se guarda.
- Marcarlo como hecho o dejarlo pendiente con un clic sobre la fila. El nombre se tacha cuando está hecho.
- Eliminarlo con el botón **Eliminar**.
- Ver tres contadores: **Total**, **Hechos** y **Faltan**.
- Conservar la lista en `localStorage` (clave `habitos`) al recargar la página.
- Acomodar el tablero en pantallas angostas: los contadores y el formulario se apilan.

## Tecnologías

- HTML5
- CSS3
- [Bootstrap 5.3](https://getbootstrap.com/) (hoja de estilos por CDN)
- JavaScript (ES6+): funciones flecha, desestructuración, render del DOM y un solo listener por delegación en la lista
- Git y GitHub

## Cómo ejecutarlo en local

Hace falta un navegador actual. No hay dependencias ni paso de instalación.

```bash
git clone https://github.com/Scorpwik/tracker-de-habitos.git
cd tracker-de-habitos
```

Abrir `index.html` en el navegador.

Si se prefiere un servidor estático:

```bash
python3 -m http.server 8000
```

Luego entrar a [http://localhost:8000](http://localhost:8000).

En VS Code, Live Server puede usar el puerto `5501` definido en `.vscode/settings.json`.

## Estructura

```text
tracker-de-habitos/
├── index.html    # marcado de la página
├── style.css     # tablero y diseño adaptable
├── app.js        # hábitos, contadores y localStorage
├── README.md
└── .vscode/
    └── settings.json
```

Las hojas y el script se enlazan con rutas relativas (`style.css`, `app.js`), así el sitio publicado en GitHub Pages resuelve bien bajo `/tracker-de-habitos/`.

## Autor

Joshua Lozada — [Scorpwik](https://github.com/Scorpwik)
