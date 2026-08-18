# Configuración e Instalación de PostgreSQL con Docker y DataGrip

* **Estudiante:** Luis Eduardo Flores Garcia
* **Descripción:** Documentación del despliegue de PostgreSQL en Docker, conexión desde DataGrip y creación de la base de datos.

---

## 🚀 1. Ejecución de PostgreSQL en Docker

Para desplegar el contenedor de PostgreSQL, se ejecutó el siguiente comando en la terminal:

```bash
docker run --name postgres-db -e POSTGRES_PASSWORD=yourpassword -p 5432:5432 -d postgres
```

### Comprobación de estado
Para verificar que el contenedor esté activo y corriendo correctamente:
```bash
docker ps
```

---

## 🛠️ 2. Configuración de DataGrip

Pasos realizados para conectar JetBrains DataGrip con el servidor PostgreSQL:

1. En **DataGrip**, abrir el panel **Database Explorer** e ir a `+` > **Data Source** > **PostgreSQL**.
2. Configurar los siguientes parámetros de conexión:
   * **Host:** `localhost`
   * **Port:** `5432`
   * **User:** `postgres`
   * **Password:** `yourpassword`
   * **Database:** `postgres`
3. Descargar el controlador correspondiente (**Download Driver**).
4. Presionar **Test Connection** para comprobar la conectividad exitosa (`Succeeded`).
5. Guardar la configuración haciendo clic en **OK**.

---

## 🗄️ 3. Creación de la Base de Datos

1. Abrir la consola SQL (`console [postgres@localhost]`).
2. Ejecutar la sentencia SQL:

```sql
CREATE DATABASE mi_base_datos;
```

3. Confirmar la ejecución exitosa en la consola inferior (`completed`).
4. Hacer clic en el botón de **Refresh (🔄)** en el *Database Explorer* y desplegar el menú de la conexión para visualizar la nueva base de datos **`mi_base_datos`**.