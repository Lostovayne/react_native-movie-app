# Proyecto React Native con Expo, TypeScript y NativeWind

Este es un proyecto de plantilla para aplicaciones React Native utilizando Expo, TypeScript para un tipado fuerte, y NativeWind para estilizado con clases de utilidad tipo Tailwind CSS.

[![React Native](https://img.shields.io/badge/React%20Native-20232A?style=for-the-badge&logo=react&logoColor=61DAFB)](https://reactnative.dev/)
[![Expo](https://img.shields.io/badge/Expo-000020?style=for-the-badge&logo=expo&logoColor=white)](https://expo.dev/)
[![TypeScript](https://img.shields.io/badge/TypeScript-007ACC?style=for-the-badge&logo=typescript&logoColor=white)](https://www.typescriptlang.org/)
[![Tailwind CSS](https://img.shields.io/badge/Tailwind_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://tailwindcss.com/)
[![NativeWind](https://img.shields.io/badge/NativeWind-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white)](https://www.nativewind.dev/)

## Tabla de Contenidos

- [Características](#características)
- [Tech Stack](#tech-stack)
- [Prerrequisitos](#prerrequisitos)
- [Instalación y Configuración](#instalación-y-configuración)
- [Ejecutar el Proyecto](#ejecutar-el-proyecto)
- [Estructura de Carpetas](#estructura-de-carpetas)
- [Scripts Disponibles](#scripts-disponibles)
- [Estilizado](#estilizado)
- [Linting y Formateo](#linting-y-formateo)
- [Contribuciones](#contribuciones)
- [Licencia](#licencia)

## Características

- **Desarrollo Multiplataforma**: Construye para iOS, Android y Web con una única base de código gracias a Expo.
- **Tipado Fuerte**: Código más robusto y mantenible con TypeScript.
- **Estilizado Moderno**: Utiliza NativeWind para aplicar clases de utilidad de Tailwind CSS directamente en tus componentes React Native.
- **Componentes Reutilizables**: Estructura base con componentes temáticos y ejemplos.
- **Configuración Lista**: Incluye configuraciones para Babel, Metro, ESLint y TypeScript.

## Tech Stack

- **React Native**: Framework para construir aplicaciones móviles nativas con JavaScript y React.
- **Expo**: Plataforma y conjunto de herramientas para facilitar el desarrollo y despliegue de aplicaciones React Native.
- **TypeScript**: Superset de JavaScript que añade tipado estático opcional.
- **NativeWind**: Permite usar clases de utilidad de Tailwind CSS en React Native.
- **Tailwind CSS**: Framework CSS de utilidad para un diseño rápido y personalizable.
- **ESLint**: Herramienta para identificar y reportar patrones problemáticos en el código JavaScript/TypeScript.

## Prerrequisitos

Antes de comenzar, asegúrate de tener instalado lo siguiente en tu sistema:

- [Node.js](https://nodejs.org/) (versión LTS recomendada, ej. 18.x o superior)
- [npm](https://www.npmjs.com/) (viene con Node.js) o [Yarn](https://yarnpkg.com/)
- [Expo CLI](https://docs.expo.dev/get-started/installation/):
  ```bash
  npm install -g expo-cli
  # o
  yarn global add expo-cli
  ```
- Para desarrollo en iOS: [Xcode](https://developer.apple.com/xcode/) (solo en macOS)
- Para desarrollo en Android: [Android Studio](https://developer.android.com/studio) y configuración del emulador/dispositivo.

## Instalación y Configuración

Sigue estos pasos para configurar el proyecto localmente:

1.  **Clona el repositorio (si aplica) o descarga los archivos del proyecto.**

2.  **Navega al directorio del proyecto:**
    ```bash
    cd tu-proyecto-react-native
    ```

3.  **Instala las dependencias:**
    Usando npm:
    ```bash
    npm install
    ```
    O usando Yarn:
    ```bash
    yarn install
    ```

4.  **(Opcional) Si es la primera vez o después de cambios en `tailwind.config.js`, genera los estilos de NativeWind:**
    NativeWind generalmente funciona en tiempo de ejecución, pero si encuentras problemas, asegúrate de que tu configuración de Tailwind esté correcta.

## Ejecutar el Proyecto

Una vez instaladas las dependencias, puedes iniciar el servidor de desarrollo de Expo:

```bash
npm start
# o
yarn start
```

Esto abrirá Expo DevTools en tu navegador. Desde allí, puedes:

-   **Ejecutar en un dispositivo iOS/Android:** Escanea el código QR con la aplicación Expo Go (disponible en App Store y Google Play Store).
-   **Ejecutar en un emulador de iOS:** Presiona `i` en la terminal.
-   **Ejecutar en un emulador/dispositivo Android:** Presiona `a` en la terminal.
-   **Ejecutar en el navegador web:** Presiona `w` en la terminal.

### Scripts específicos de plataforma:

También puedes usar los scripts definidos en `package.json`:

-   Para Android:
    ```bash
    npm run android
    # o
    yarn android
    ```
-   Para iOS:
    ```bash
    npm run ios
    # o
    yarn ios
    ```
-   Para Web:
    ```bash
    npm run web
    # o
    yarn web
    ```

## Estructura de Carpetas

La estructura principal del proyecto es la siguiente:

```
.
├── app/                # Contiene las pantallas y la navegación principal (Expo Router)
│   ├── _layout.tsx     # Layout principal de la aplicación
│   ├── global.css      # Estilos globales (si se usan con NativeWind v4+)
│   └── index.tsx       # Pantalla de inicio
├── assets/             # Recursos estáticos como fuentes e imágenes
│   ├── fonts/
│   └── images/
├── components/         # Componentes reutilizables de la UI
│   └── ui/             # Componentes de UI más específicos o atómicos
├── constants/          # Constantes globales (ej. colores, configuraciones)
│   └── Colors.ts       # Esquema de colores
├── hooks/              # Hooks personalizados de React
├── scripts/            # Scripts de utilidad para el proyecto
├── .gitignore
├── app.json            # Configuración de la aplicación Expo
├── babel.config.js     # Configuración de Babel
├── eslint.config.js    # Configuración de ESLint (nuevo formato plano)
├── metro.config.js     # Configuración de Metro Bundler
├── nativewind-env.d.ts # Definiciones de tipo para NativeWind
├── package.json        # Dependencias y scripts del proyecto
├── tailwind.config.js  # Configuración de Tailwind CSS para NativeWind
├── tsconfig.json       # Configuración de TypeScript
└── README.md           # Este archivo
```

-   **`app/`**: Directorio principal para las rutas y pantallas de la aplicación, gestionado por `expo-router`.
-   **`assets/`**: Almacena fuentes, imágenes y otros activos estáticos.
-   **`components/`**: Contiene componentes de UI reutilizables en toda la aplicación.
-   **`constants/`**: Define valores constantes como temas de color, configuraciones globales, etc.
-   **`hooks/`**: Para hooks personalizados de React que encapsulan lógica reutilizable.
-   **`scripts/`**: Scripts de utilidad, como `reset-project.js`.

## Scripts Disponibles

En el archivo `package.json`, encontrarás varios scripts útiles:

-   `"start"`: Inicia el servidor de desarrollo de Expo.
-   `"android"`: Inicia la aplicación en un emulador/dispositivo Android.
-   `"ios"`: Inicia la aplicación en un emulador/dispositivo iOS.
-   `"web"`: Inicia la aplicación en un navegador web.
-   `"lint"`: Ejecuta ESLint para analizar el código en busca de errores y problemas de estilo.
-   `"reset-project"`: Ejecuta el script `scripts/reset-project.js`.

## Estilizado

Este proyecto utiliza **NativeWind** para el estilizado, lo que permite usar clases de utilidad de Tailwind CSS directamente en los componentes de React Native.

-   **Configuración de Tailwind**: Se encuentra en `tailwind.config.js`.
-   **Uso**: Simplemente añade clases de Tailwind a la prop `className` de tus componentes.
    ```tsx
    import { Text, View } from 'react-native';

    export default function MyComponent() {
      return (
        <View className="p-4 bg-blue-500 rounded-lg">
          <Text className="text-white text-lg font-bold">Hola NativeWind!</Text>
        </View>
      );
    }
    ```
-   **Estilos Globales**: Para estilos que necesitas aplicar globalmente o para configurar NativeWind v4+, puedes usar `app/global.css`.

Los colores base y temáticos se definen en `constants/Colors.ts` y pueden ser utilizados en conjunto con NativeWind o estilos directos.

## Linting y Formateo

-   **ESLint**: Configurado en `eslint.config.js` para mantener la calidad y consistencia del código. Puedes ejecutar el linter con:
    ```bash
    npm run lint
    # o
    yarn lint
    ```
-   **Prettier (Recomendado)**: Aunque no está explícitamente configurado en `package.json` como un script, se recomienda usar Prettier para el formateo automático del código. Puedes integrarlo con tu editor o ejecutarlo manualmente.

## Contribuciones

Las contribuciones son bienvenidas. Si deseas contribuir, por favor:

1.  Haz un fork del repositorio.
2.  Crea una nueva rama (`git checkout -b feature/nueva-funcionalidad`).
3.  Realiza tus cambios y haz commit (`git commit -m 'Añade nueva funcionalidad'`).
4.  Empuja tus cambios a la rama (`git push origin feature/nueva-funcionalidad`).
5.  Abre un Pull Request.

## Licencia

Este proyecto está bajo la Licencia MIT. Consulta el archivo `LICENSE` (si existe) para más detalles, o considera añadir uno.

---

¡Feliz codificación! ✨