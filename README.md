# Hierro — app privada de gimnasio

Aplicación web progresiva (PWA) para Android. No tiene cuentas, perfiles, feed, seguidores, anuncios ni analítica. Las rutinas y el historial se guardan en el almacenamiento local del navegador en el dispositivo.

## Funciones
- Rutinas editables y ejercicios predeterminados o personalizados.
- Entrenamiento libre o desde una rutina.
- Registro de peso, repeticiones y series completadas.
- Temporizador de descanso ajustable.
- Historial, repetición de sesiones y eliminación de registros.
- Mejores marcas por ejercicio y registro/gráfica de peso corporal.
- Exportación e importación de copia de seguridad JSON.
- Interfaz adaptable a móvil y funcionamiento sin conexión tras la primera carga.

## Instalación recomendada: GitHub Pages (gratis)
La instalación PWA requiere una dirección HTTPS (GitHub Pages proporciona HTTPS). No abras `index.html` desde el gestor de archivos si quieres instalarla como app.

1. En un ordenador, entra en https://github.com/ y crea una cuenta si no tienes.
2. Crea un repositorio nuevo, por ejemplo `hierro-gym`. Puedes dejarlo público si vas a usar GitHub Pages gratis. No pongas datos personales en el repositorio: solo contiene el código de la app, no tus entrenamientos.
3. Sube todos los archivos de esta carpeta a la raíz del repositorio: `index.html`, `styles.css`, `app.js`, `manifest.webmanifest`, `sw.js`, `icon.svg`, `icon-192.png`, `icon-512.png`.
4. En el repositorio abre **Settings → Pages**.
5. En **Build and deployment**, elige **Deploy from a branch**, selecciona `main` y `/ (root)`, y pulsa **Save**.
6. Espera a que GitHub Pages publique el sitio. La URL tendrá un formato parecido a `https://TU-USUARIO.github.io/hierro-gym/`.
7. Abre esa URL en Chrome en tu Pixel. Espera a que cargue por completo una vez.
8. En Chrome, pulsa **⋮ → Añadir a pantalla de inicio** o **Instalar aplicación** (el texto puede variar). Confirma.
9. Abre Hierro desde el icono instalado. Después de la primera carga, la app debería poder abrirse sin conexión.

## Privacidad y límites
- El sitio estático aloja solo los archivos de la app; no recibe tus entrenamientos. La app no implementa telemetría ni llamadas de red a servicios de datos.
- Google Fonts está declarado en el CSS para la tipografía. Si prefieres cero solicitudes a terceros incluso durante la primera carga, elimina la primera línea `@import` de `styles.css`; se usará una fuente de sistema.
- Los datos viven en el almacenamiento del navegador de esa instalación. Borrar los datos del sitio, desinstalar el navegador o cambiar de dispositivo puede eliminarlos. Exporta copias regularmente desde **Privacidad**.
- La copia JSON contiene tu historial. Guárdala en un lugar privado.
- Esta versión no sincroniza entre dispositivos ni cifra el almacenamiento local con una contraseña.
- La app es una primera versión funcional, no una copia exacta ni afiliada a Hevy.

## Prueba local de desarrollo
Puedes abrir `index.html` en un navegador para probar muchas funciones, pero el modo PWA y el caché offline requieren servir el sitio por HTTPS o `localhost`.
