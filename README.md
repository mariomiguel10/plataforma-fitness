# Plataforma de Fitness Avanzada

Una aplicación web completa para gestionar perfiles de fitness, generar planes nutricionales y de entrenamiento personalizados.

## Características

- ✅ Gestión de múltiples perfiles de usuario
- ✅ Cálculo automático de macros nutricionales
- ✅ Generación de menús semanales personalizados
- ✅ Planes de entrenamiento adaptados al nivel de actividad
- ✅ Seguimiento de progreso con gráficos
- ✅ Generación de recetas con IA (Google Gemini)
- ✅ Exportación a PDF
- ✅ Interfaz responsive y moderna

## Configuración Requerida

### 1. Firebase Configuration

Para que la aplicación funcione, necesitas configurar Firebase:

1. Ve a [Firebase Console](https://console.firebase.google.com/)
2. Crea un nuevo proyecto
3. Habilita Authentication (Anonymous)
4. Habilita Firestore Database
5. Obtén tu configuración de Firebase

Reemplaza la configuración en `index.html` (líneas 175-183):

```javascript
const firebaseConfig = {
    apiKey: "tu-api-key-real",
    authDomain: "tu-proyecto.firebaseapp.com",
    projectId: "tu-proyecto-id",
    storageBucket: "tu-proyecto.appspot.com",
    messagingSenderId: "123456789",
    appId: "tu-app-id"
};
```

### 2. Google Gemini API Key

Para usar la generación de recetas con IA:

1. Ve a [Google AI Studio](https://makersuite.google.com/app/apikey)
2. Crea una nueva API key
3. Reemplaza `"TU_API_KEY_DE_GEMINI_AQUI"` en la línea 456 del código

## Instalación

1. Clona o descarga el proyecto
2. Configura Firebase y Gemini API como se indica arriba
3. Abre `index.html` en tu navegador
4. ¡Listo para usar!

## Uso

1. **Crear Perfil**: Ingresa tus datos personales y objetivos
2. **Generar Plan**: Personaliza exclusiones y días sin cena
3. **Seguir Plan**: Consulta tu menú diario y rutina de ejercicios
4. **Registrar Progreso**: Anota tu peso para ver tu evolución
5. **Descargar PDF**: Exporta tu plan completo

## Estructura del Proyecto

```
plataforma-fitness/
├── index.html          # Aplicación principal
└── README.md          # Este archivo
```

## Tecnologías Utilizadas

- **Frontend**: HTML5, CSS3 (Tailwind CSS), JavaScript ES6+
- **Backend**: Firebase (Authentication, Firestore)
- **IA**: Google Gemini API
- **Gráficos**: Chart.js
- **PDF**: jsPDF + AutoTable

## Notas Importantes

- La aplicación funciona completamente en el navegador
- Los datos se almacenan en Firebase Firestore
- Se requiere conexión a internet para funcionar
- La generación de recetas con IA es opcional

## Solución de Problemas

### Error de Firebase
- Verifica que la configuración de Firebase sea correcta
- Asegúrate de que Authentication y Firestore estén habilitados

### Error de API Key
- Si no configuras la API key de Gemini, la funcionalidad de IA mostrará un mensaje explicativo
- La aplicación funciona completamente sin la API key

### Problemas de Carga
- Verifica tu conexión a internet
- Revisa la consola del navegador para errores específicos 