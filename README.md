# Codelab: Cómo usar Hilt en tu app para Android

## Descripción del proyecto
Este repositorio contiene la solución completada del codelab oficial de Android Developers **"Cómo usar Hilt en tu app para Android"** (*Using Hilt in your Android app*).

La aplicación `LoggingApp` registra las interacciones de los botones en una base de datos local utilizando **Room** y muestra el historial ordenado por fecha y hora.

## Conceptos practicados
* **Configuración de Hilt:** Integración del plugin de Hilt en Gradle y uso de `@HiltAndroidApp` en `LogApplication`.
* **Inyección de dependencias en Android:** Uso de `@AndroidEntryPoint` e `@Inject` en `MainActivity`, `ButtonsFragment` y `LogsFragment`, eliminando el uso manual de `ServiceLocator`.
* **Alcance de instancias:** Uso de `@Singleton` en `LoggerLocalDataSource` para mantener una única instancia compartida en toda la aplicación.
* **Módulos de Hilt (`@Module` y `@InstallIn`):**
  * `DatabaseModule` con `@Provides` para proveer `AppDatabase` (Room) y `LogDao`.
  * `NavigationModule` con `@Binds` para vincular la interfaz `AppNavigator` con `AppNavigatorImpl`.

## Problema encontrado y solución
* **Problema:** Al sincronizar el proyecto por primera vez en Android Studio, Gradle falló con el error `Your project path contains non-ASCII characters` porque la ruta contenía una tilde (`Plataformas Móviles`).
* **Solución:** Se cerró Android Studio, se renombró la carpeta sin tildes (`Plataformas Moviles`) y se volvió a sincronizar Gradle exitosamente.

## Capturas de pantalla
<img width="498" height="886" alt="image" src="https://github.com/user-attachments/assets/1ef6a5de-fe4a-4174-bb22-bf038fa19dde" />

<img width="553" height="1081" alt="image" src="https://github.com/user-attachments/assets/46885566-3f11-4688-8be6-118161fdca63" />


