# Monedero Virtual: cómo abrirlo y ejecutarlo

## 1. Instalar un JDK que traiga JavaFX (una sola vez)

Si aparece el error `package javafx.application does not exist`, es porque el Java instalado no trae JavaFX.

1. Entrar a **https://www.azul.com/downloads** y filtrar:
   - **Java Version:** 17 (LTS)
   - **Operating System:** Windows
   - **Architecture:** x86 64-bit
   - **Java Package:** **JDK FX** (tiene que decir FX)
2. Descargar el **.msi** e instalarlo. Normalmente queda en `C:\Program Files\Zulu\zulu-17...`.

## 2. Abrir en IntelliJ IDEA

1. Descomprimir el `.zip`.
2. **File → Open** y escoger la carpeta **`MonederoVirtual`**, la que tiene adentro `src`, `datos` y `documentacion`. Luego **Trust Project**.
3. **File → Project Structure → Project → SDK**:
   - **Add SDK → JDK…** (o *Add JDK from disk*) y escoger la carpeta del JDK de Azul FX (la que tiene `bin`);
   - **Language level:** 17;
   - **Apply → OK**.
4. Ejecutar: arriba a la derecha está la configuración **Main**; se le da al **▶ verde**. También se puede abrir `src/main/java/co/edu/uniquindio/poo/app/Main.java` y darle ▶.

**Si siguen errores en rojo:** **File → Invalidate Caches → Invalidate and Restart**.

## 3. Abrir en VS Code

1. Abrir la carpeta `MonederoVirtual` y confiar en ella ("Trust").
2. En `.vscode/settings.json`, cambiar la ruta del JDK por la del JDK de Azul FX de su computador.
3. Abrir `Main.java` y darle **Run**.

## Estructura

```
src/main/java/co/edu/uniquindio/poo/app/      Main y MonederoController
src/main/java/co/edu/uniquindio/poo/model/    Todas las clases del negocio
src/main/resources/co/edu/uniquindio/poo/app/ MonederoVista.fxml (Scene Builder)
datos/                                        Archivos CSV con la información
documentacion/                                UML y explicación del código y del proyecto
```
