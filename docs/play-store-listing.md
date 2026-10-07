# Play Store listing — Paralgo (draft, paste into Play Console)

Default listing language: **Español**. All texts below are within Play's character limits.

## Título (≤30)

```
Paralgo: reflexión diaria
```

## Descripción corta (≤80)

```
Registra lo bueno y lo desagradable de tu día y analízalo. 100% offline.
```

## Descripción completa (≤4000)

```
Paralgo es tu espacio diario de reflexión personal.

Cada día puedes registrar tus agradecimientos (lo bueno que viviste) y tus desagrados (lo que te molestó). Por cada desagrado, Paralgo te guía con un análisis sencillo, paso a paso:

• ¿Irrelevante o relevante? Si es irrelevante y puntual, el análisis simplemente termina.
• ¿Es crónico? Lo que se repite en el tiempo se trata como relevante.
• ¿Es modificable? Si no lo es, la conclusión es tomar una decisión.
• Si sí lo es, defines si el cambio depende de ti, de tu pareja o de ambos, y cierras con un plan de cambios con estrategias y cronograma.

Al terminar tu día tienes un resumen claro y, con el tiempo, tu historial completo para mirar hacia atrás.

Privacidad total:
• Sin cuentas, sin permisos, sin publicidad y sin conexión a ningún servidor.
• Toda tu información queda únicamente en tu dispositivo; ni siquiera se respalda en la nube.
• Sin analíticas ni rastreadores de ningún tipo.

Si desinstalas la aplicación, todo desaparece con ella.
```

## Console settings checklist

| Field | Answer |
|---|---|
| Categoría | Estilo de vida (Apps) |
| Público objetivo | 18+ (no dirigido a menores) |
| Clasificación de contenido | Cuestionario completado con "no" en todo → Para todos / Everyone |
| Anuncios | No contiene anuncios |
| Compras | Sin compras en la app |
| Seguridad de datos | No se recopilan datos; no se comparten datos; no se transfieren datos. Todo "No". |
| Eliminación de datos | No aplica (no se recopila nada) |
| Correo de contacto | (email pending) |
| URL política de privacidad | GitHub Pages URL (pending publish of docs/index.md) |
| Distribución | Todos los países (o LatAm + España — a tu criterio) |
| Acceso de la app | Completamente gratuita, sin restricciones |

## Graphics needed

- **Icono 512×512 PNG** (Play listing) — currently the adaptive icon is teal with a white ring; export or regenerate.
- **Recurso destacado 1024×500** (feature graphic).
- **Capturas: 4–6** (teléfono), ideally: Inicio, Agradecimientos con ítems,
  Desagrados con un resultado, una pregunta del árbol, una pantalla de resultado, Historial.
  Capture with the emulator's camera (screenshot) button while running the app.

## Release sequence (user steps)

1. Generate upload keystore (never commit it; back it up off-machine):
   `keytool -genkeypair -v -keystore paralgo-upload.jks -alias upload -keyalg RSA -keysize 2048 -validity 10000`
2. Build → Generate Signed App Bundle in Android Studio → `app-release.aab`.
3. Push repo to GitHub (public); enable Settings → Pages → main branch, `/docs` → paste the URL into Console.
   enable Settings → Pages → main branch, `/docs` → paste the URL into Console.
4. Create app in Play Console, paste the texts/graphics above, complete the checklist.
5. Upload AAB to Internal testing; install on a real device; verify.
6. New personal developer accounts: run a closed test with ≥12 testers opted in
   continuously for 14 days before production access (verify current numbers in Console).
7. Apply for production → submit for review (first review may take several days).
