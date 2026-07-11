# Publicar la web con GitHub + Netlify (auto-deploy)

Objetivo: que cada cambio se publique **solo** en `universo-guguiarte.netlify.app`, sin arrastrar zips.
Esta carpeta (`guguiarte-web`) es la web completa y será el repositorio.

---

## Paso 1 · Instala GitHub Desktop (una vez)
Descarga e instala **GitHub Desktop** desde https://desktop.github.com y entra con tu cuenta de GitHub.

## Paso 2 · Convierte esta carpeta en repositorio
1. En GitHub Desktop: **File → Add local repository…**
2. Elige esta carpeta: `guguiarte-web`.
3. Si te dice que no es un repositorio, pulsa **"create a repository"** (Initialize).
4. Pulsa **Publish repository** (arriba a la derecha).
   - Nombre sugerido: `universo-guguiarte`
   - Puedes dejarlo privado (marca "Keep this code private").

Ya tienes el código en tu GitHub.

## Paso 3 · Conecta Netlify al repositorio
1. Entra en https://app.netlify.com
2. **Add new site → Import an existing project → Deploy with GitHub**.
3. Autoriza GitHub y elige el repo `universo-guguiarte`.
4. Configuración (es HTML estático, muy simple):
   - **Build command:** (déjalo vacío)
   - **Publish directory:** `.` (un punto) o déjalo vacío
5. **Deploy site**.

> Nota: si quieres que sea el MISMO sitio de antes (`universo-guguiarte.netlify.app`),
> puedes borrar el sitio anterior o, en el sitio actual, ir a
> **Site configuration → Build & deploy → Link repository** y enlazar este repo.

## Paso 4 · El día a día (así se actualiza)
Cuando yo (o tú) cambie algo en esta carpeta:
1. Abre **GitHub Desktop** → verás los cambios listados.
2. Escribe una nota corta abajo a la izquierda y pulsa **Commit to main**.
3. Pulsa **Push origin** (arriba).
4. Netlify lo detecta y **publica solo** en ~1 minuto.

Sin zips. Sin arrastrar. Solo Commit → Push.

---

## Importante
A partir de ahora, **esta carpeta `guguiarte-web` es la oficial**. Los cambios se hacen aquí.
La carpeta `netlify-guguiarte` (y su zip) se pueden borrar cuando esto funcione.
