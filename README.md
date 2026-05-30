# Visor WebAR · Modelo 3D

Página web para visualizar un modelo 3D en **Realidad Aumentada** a tamaño real, directamente desde el navegador del celular. Construida con [Google Model Viewer](https://modelviewer.dev/) y lista para desplegar en GitHub Pages.

## Estructura

```
.
├── index.html       # Visor completo: preview 3D + AR + instrucciones + QR
├── lanzar.html      # Lanzador directo: un solo botón gigante → AR inmediato
├── models/
│   ├── modelo.glb   # Modelo para Android / WebXR (Scene Viewer)
│   └── modelo.usdz  # Modelo para iOS (AR Quick Look)
└── .nojekyll        # Evita que GitHub Pages procese los archivos
```

## Cómo usar

1. Abre la URL desplegada **desde un celular**.
2. Pulsa **“Ver en mi espacio”** (o entra directamente a `lanzar.html`).
3. Apunta la cámara al piso y toca para colocar el modelo.

## Compatibilidad

| Plataforma | Navegador | Tecnología |
|---|---|---|
| Android | Chrome + Google Play Services for AR | Scene Viewer / WebXR |
| iOS 12+ | Safari | AR Quick Look |
| Escritorio | Chrome, Edge, Firefox, Safari | Solo preview 3D (sin AR) |

## Desplegar en GitHub Pages

1. Push a un repo de GitHub.
2. *Settings → Pages → Deploy from branch → `main` / root*.
3. La URL será `https://<usuario>.github.io/<repo>/`.

> ⚠️ AR requiere **HTTPS**. GitHub Pages lo provee automáticamente.

## Probar en local

```bash
python3 -m http.server 8000
```

Para probar AR desde el celular en local necesitas HTTPS (usa `ngrok http 8000` o similar).

## Créditos

- Visor: [Google Model Viewer](https://modelviewer.dev/)
