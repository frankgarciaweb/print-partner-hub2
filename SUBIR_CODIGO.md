# 📤 Cómo Subir el Código con tu Token

## Método 1: Usar el Token en la URL (Más Fácil)

Ejecuta este comando reemplazando `TU_TOKEN_AQUI` con el token que copiaste:

```bash
git remote set-url origin https://TU_TOKEN_AQUI@github.com/frankgarciaweb/print-partner-hub2.git
```

**Ejemplo:**
Si tu token es `ghp_abc123xyz`, el comando sería:
```bash
git remote set-url origin https://ghp_abc123xyz@github.com/frankgarciaweb/print-partner-hub2.git
```

Luego ejecuta:
```bash
git push -u origin main
```

---

## Método 2: Cuando Git Pida Credenciales

Si prefieres que Git te pregunte:

1. Ejecuta: `git push -u origin main`
2. Cuando aparezca una ventana pidiendo credenciales:
   - **Username:** `frankgarciaweb`
   - **Password:** Pega tu token (NO tu contraseña de GitHub)
3. Marca "Remember my credentials" si quieres
4. Haz clic en OK

---

## Método 3: Usar GitHub Desktop (Más Visual)

1. Descarga GitHub Desktop: https://desktop.github.com
2. Instálalo y conéctate con tu cuenta de GitHub
3. File → Add Local Repository
4. Selecciona tu carpeta del proyecto
5. Haz clic en "Publish repository"
6. ¡Listo!

---

## ✅ Después de Subir

Una vez que el código esté en GitHub, ve a Vercel y despliega:
1. https://vercel.com
2. Sign Up con GitHub
3. Add New Project
4. Selecciona `print-partner-hub2`
5. Deploy

¡Y tendrás tu sitio en línea!

