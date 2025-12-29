# 🔐 Solución: Problema de Autenticación con GitHub

## Problema
Git está intentando usar credenciales de otro usuario (`publicidadblue`) y no tiene permisos para subir a tu repositorio.

## ✅ Solución: Usar Token de Acceso Personal

### Paso 1: Crear Token en GitHub

1. Ve a GitHub.com e inicia sesión
2. Haz clic en tu foto de perfil (arriba derecha) → **Settings**
3. En el menú lateral izquierdo, ve a **Developer settings** (al final)
4. Haz clic en **Personal access tokens** → **Tokens (classic)**
5. Haz clic en **Generate new token** → **Generate new token (classic)**
6. Configuración:
   - **Note:** `Vercel Deploy` (o cualquier nombre)
   - **Expiration:** 90 days (o el que prefieras)
   - **Select scopes:** Marca **repo** (esto dará todos los permisos de repositorio)
7. Haz clic en **Generate token** (abajo)
8. **⚠️ IMPORTANTE:** Copia el token inmediatamente (solo se muestra una vez)
   - Se verá algo como: `ghp_xxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxxx`

### Paso 2: Usar el Token para Subir Código

**Opción A: Usar el token directamente**

Cuando Git te pida usuario y contraseña:
- **Username:** `frankgarciaweb`
- **Password:** Pega el token que copiaste (NO tu contraseña de GitHub)

**Opción B: Configurar Git Credential Manager**

Ejecuta estos comandos en PowerShell:

```powershell
# Configurar el usuario
git config --global user.name "frankgarciaweb"
git config --global user.email "tu-email@ejemplo.com"

# Limpiar credenciales guardadas
git credential-manager-core erase
# O si no funciona:
cmdkey /list
# Busca entradas de github.com y elimínalas con:
# cmdkey /delete:git:https://github.com
```

Luego intenta hacer push de nuevo. Cuando te pida credenciales:
- Usuario: `frankgarciaweb`
- Contraseña: Pega tu token

### Paso 3: Subir el Código

```bash
git push -u origin main
```

---

## 🚀 Alternativa: Desplegar Directamente desde GitHub

Si prefieres, puedes:

1. **Subir manualmente a GitHub:**
   - Ve a tu repositorio: https://github.com/frankgarciaweb/print-partner-hub2
   - Haz clic en "uploading an existing file"
   - Arrastra todos los archivos de tu proyecto
   - Haz commit

2. **O usar GitHub Desktop:**
   - Descarga GitHub Desktop desde: https://desktop.github.com
   - Conecta con tu cuenta
   - Agrega el repositorio
   - Haz commit y push desde la interfaz gráfica

---

## 📝 Después de Subir a GitHub

Una vez que el código esté en GitHub, despliega en Vercel:

1. Ve a [vercel.com](https://vercel.com)
2. Sign Up / Login con GitHub
3. Add New Project
4. Selecciona `print-partner-hub2`
5. Deploy

¡Y listo! Tu sitio estará en línea.

