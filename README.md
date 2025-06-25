<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    
    <!-- Metadatos para SEO y Compartir -->
    <title>EcoBuild | Diseña un Futuro Sostenible</title>
    <meta name="description" content="EcoBuild es la aplicación líder para arquitectos y diseñadores que optimiza el uso de materiales sostenibles como Sugarcrete mediante IA, simulación 3D y análisis de costos.">
    <meta name="keywords" content="EcoBuild, Sugarcrete, arquitectura sostenible, construcción ecológica, diseño IA, BIM, AR en arquitectura">
    <meta name="author" content="EcoBuild Inc.">

    <!-- Open Graph para Redes Sociales -->
    <meta property="og:title" content="EcoBuild | Diseña un Futuro Sostenible">
    <meta property="og:description" content="Optimiza tus diseños con materiales sostenibles, IA y simulación 3D/AR.">
    <meta property="og:image" content="https://placehold.co/1200x630/2c3e50/ffffff?text=EcoBuild">
    <meta property="og:url" content="https://ecobuild-app.com">
    <meta property="og:type" content="website">

    <!-- Twitter Card -->
    <meta name="twitter:card" content="summary_large_image">
    <meta name="twitter:title" content="EcoBuild | Diseña un Futuro Sostenible">
    <meta name="twitter:description" content="Optimiza tus diseños con materiales sostenibles, IA y simulación 3D/AR.">
    <meta name="twitter:image" content="https://placehold.co/1200x630/2c3e50/ffffff?text=EcoBuild">

    <!-- Favicon (usando un emoji SVG para simplicidad) -->
    <link rel="icon" href="data:image/svg+xml,<svg xmlns=%22http://www.w3.org/2000/svg%22 viewBox=%220 0 100 100%22><text y=%22.9em%22 font-size=%2290%22>🌿</text></svg>">

    <!-- Tailwind CSS -->
    <script src="https://cdn.tailwindcss.com"></script>

    <!-- Google Fonts: Inter -->
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700;800&display=swap" rel="stylesheet">
    
    <!-- Three.js para la demo 3D -->
    <script async src="https://unpkg.com/es-module-shims@1.6.3/dist/es-module-shims.js"></script>
    <script type="importmap">
    {
        "imports": {
        "three": "https://cdn.jsdelivr.net/npm/three@0.155.0/build/three.module.js",
        "three/addons/": "https://cdn.jsdelivr.net/npm/three@0.155.0/examples/jsm/"
        }
    }
    </script>

    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #F3F4F6; /* Gris claro de fondo */
        }
        .text-gradient {
            background: -webkit-linear-gradient(45deg, #10B981, #3B82F6);
            -webkit-background-clip: text;
            -webkit-text-fill-color: transparent;
        }
        .faq-item .answer {
            display: none;
            transition: all 0.3s ease-in-out;
        }
        .faq-item.open .answer {
            display: block;
        }
        .faq-item.open .icon-plus { display: none; }
        .faq-item:not(.open) .icon-minus { display: none; }
    </style>
</head>
<body class="text-gray-800">

    <!-- =========== Header =========== -->
    <header id="header" class="bg-white/80 backdrop-blur-lg fixed top-0 left-0 w-full z-40 transition-all duration-300 shadow-sm">
        <div class="container mx-auto px-6 py-4 flex justify-between items-center">
            <a href="#" class="flex items-center space-x-2">
                <svg class="h-8 w-8 text-emerald-500" xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5"></path></svg>
                <span class="text-2xl font-bold text-gray-800">EcoBuild</span>
            </a>
            <nav class="hidden md:flex items-center space-x-8">
                <a href="#features" class="text-gray-600 hover:text-emerald-500 transition-colors">Funcionalidades</a>
                <a href="#demo" class="text-gray-600 hover:text-emerald-500 transition-colors">Demo</a>
                <a href="#contact" class="text-gray-600 hover:text-emerald-500 transition-colors">Contacto</a>
            </nav>
            <a href="#" class="hidden md:inline-block bg-emerald-500 text-white font-semibold px-5 py-2 rounded-lg hover:bg-emerald-600 transition-all shadow-sm hover:shadow-lg transform hover:-translate-y-px">
                Registrarse
            </a>
            <button id="mobile-menu-button" class="md:hidden text-gray-700">
                <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24" xmlns="http://www.w3.org/2000/svg"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16m-7 6h7"></path></svg>
            </button>
        </div>
        <!-- Mobile Menu -->
        <div id="mobile-menu" class="hidden md:hidden px-6 pt-2 pb-4">
            <a href="#features" class="block py-2 text-gray-600 hover:text-emerald-500">Funcionalidades</a>
            <a href="#demo" class="block py-2 text-gray-600 hover:text-emerald-500">Demo</a>
            <a href="#contact" class="block py-2 text-gray-600 hover:text-emerald-500">Contacto</a>
            <a href="#" class="block w-full text-center mt-4 bg-emerald-500 text-white font-semibold px-5 py-2 rounded-lg hover:bg-emerald-600">Registrarse</a>
        </div>
    </header>

    <!-- =========== Hero Section =========== -->
    <main class="pt-24">
        <section class="container mx-auto px-6 py-20 text-center">
            <h1 class="text-4xl md:text-6xl font-extrabold text-gray-900 leading-tight">
                Diseña un <span class="text-gradient">futuro sostenible</span> con EcoBuild
            </h1>
            <p class="mt-6 max-w-2xl mx-auto text-lg text-gray-600">
                La plataforma inteligente para arquitectos y diseñadores que revoluciona la construcción con materiales ecológicos, IA y visualización avanzada.
            </p>
            <div class="mt-10 flex flex-col sm:flex-row justify-center items-center space-y-4 sm:space-y-0 sm:space-x-4">
                <a href="#demo" class="w-full sm:w-auto bg-emerald-500 text-white font-semibold px-8 py-3 rounded-lg hover:bg-emerald-600 transition-all shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                    Ver Demo Interactiva
                </a>
                <a href="#download" class="w-full sm:w-auto bg-gray-200 text-gray-800 font-semibold px-8 py-3 rounded-lg hover:bg-gray-300 transition-all shadow-lg hover:shadow-xl transform hover:-translate-y-1">
                    Descargar App
                </a>
            </div>
        </section>

        <!-- =========== Features Section =========== -->
        <section id="features" class="py-20 bg-white">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Funcionalidades Clave</h2>
                    <p class="mt-4 text-gray-600">Todo lo que necesitas para llevar tus proyectos al siguiente nivel de sostenibilidad.</p>
                </div>
                <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
                    <!-- Feature Item -->
                    <div class="bg-gray-50 p-6 rounded-lg text-center transform hover:scale-105 transition-transform duration-300 shadow-sm hover:shadow-xl">
                        <div class="inline-block p-4 bg-emerald-100 text-emerald-600 rounded-full mb-4">
                            <svg class="w-8 h-8" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="m12 3-1.45 1.45-2.52 2.52-1.45 1.45L2 12.87l7.58 7.58L15 15l2.52-2.52L21.45 8 12 3Z"/><path d="M8 16v-5.5a2.5 2.5 0 0 1 5 0V16"/><path d="M12 21a6 6 0 0 0 3.5-10.6L12 7l-3.5 3.4A6 6 0 0 0 12 21Z"/></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Recomendaciones por IA</h3>
                        <p class="text-gray-600">Optimiza materiales, costos y eficiencia energética con sugerencias inteligentes basadas en el contexto de tu proyecto.</p>
                    </div>
                    <!-- Feature Item -->
                    <div class="bg-gray-50 p-6 rounded-lg text-center transform hover:scale-105 transition-transform duration-300 shadow-sm hover:shadow-xl">
                        <div class="inline-block p-4 bg-emerald-100 text-emerald-600 rounded-full mb-4">
                           <svg class="w-8 h-8" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M21 16V8a2 2 0 0 0-1-1.73l-7-4a2 2 0 0 0-2 0l-7 4A2 2 0 0 0 3 8v8a2 2 0 0 0 1 1.73l7 4a2 2 0 0 0 2 0l7-4A2 2 0 0 0 21 16z"></path><polyline points="3.27 6.96 12 12.01 20.73 6.96"></polyline><line x1="12" y1="22.08" x2="12" y2="12"></line></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Simulación 3D y AR</h3>
                        <p class="text-gray-600">Visualiza tus diseños en 3D en tiempo real y proyéctalos en el mundo real con nuestra función de Realidad Aumentada.</p>
                    </div>
                    <!-- Feature Item -->
                    <div class="bg-gray-50 p-6 rounded-lg text-center transform hover:scale-105 transition-transform duration-300 shadow-sm hover:shadow-xl">
                        <div class="inline-block p-4 bg-emerald-100 text-emerald-600 rounded-full mb-4">
                            <svg class="w-8 h-8" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><line x1="12" y1="1" x2="12" y2="23"></line><path d="M17 5H9.5a3.5 3.5 0 0 0 0 7h5a3.5 3.5 0 0 1 0 7H6"></path></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Optimización de Costos</h3>
                        <p class="text-gray-600">Calcula automáticamente la cantidad de materiales necesarios y obtén un desglose de costos en tiempo real.</p>
                    </div>
                    <!-- Feature Item -->
                    <div class="bg-gray-50 p-6 rounded-lg text-center transform hover:scale-105 transition-transform duration-300 shadow-sm hover:shadow-xl">
                         <div class="inline-block p-4 bg-emerald-100 text-emerald-600 rounded-full mb-4">
                             <svg class="w-8 h-8" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 2L2 7l10 5 10-5-10-5z"></path><path d="M2 17l10 5 10-5"></path><path d="M2 12l10 5 10-5"></path></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Generación de Proyectos</h3>
                        <p class="text-gray-600">Ingresa datos básicos y genera planos de diseño con Sugarcrete como material principal de forma automática.</p>
                    </div>
                     <!-- Feature Item -->
                    <div class="bg-gray-50 p-6 rounded-lg text-center transform hover:scale-105 transition-transform duration-300 shadow-sm hover:shadow-xl">
                        <div class="inline-block p-4 bg-emerald-100 text-emerald-600 rounded-full mb-4">
                           <svg class="w-8 h-8" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M17.5 19H9a7 7 0 1 1 6.71-9h1.79a4.5 4.5 0 1 1 0 9Z"/><path d="M22 12a2.5 2.5 0 0 1-5 0 4.2 4.2 0 0 1-1.23-3.13 3.6 3.6 0 0 1 2.45-3.33A5 5 0 0 1 22 12Z"/></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Colaboración en la Nube</h3>
                        <p class="text-gray-600">Guarda y sincroniza proyectos en la nube para acceder desde cualquier dispositivo y colaborar con tu equipo en tiempo real.</p>
                    </div>
                     <!-- Feature Item -->
                    <div class="bg-gray-50 p-6 rounded-lg text-center transform hover:scale-105 transition-transform duration-300 shadow-sm hover:shadow-xl">
                        <div class="inline-block p-4 bg-emerald-100 text-emerald-600 rounded-full mb-4">
                            <svg class="w-8 h-8" xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M14.5 2H6a2 2 0 0 0-2 2v16a2 2 0 0 0 2 2h12a2 2 0 0 0 2-2V7.5L14.5 2z"></path><polyline points="14 2 14 8 20 8"></polyline><line x1="16" y1="13" x2="8" y2="13"></line><line x1="16" y1="17" x2="8" y2="17"></line><line x1="10" y1="9" x2="8" y2="9"></line></svg>
                        </div>
                        <h3 class="text-xl font-semibold mb-2">Análisis Post-Construcción</h3>
                        <p class="text-gray-600">Monitorea la huella de carbono, eficiencia energética y otros indicadores de sostenibilidad de tu edificio.</p>
                    </div>
                </div>
            </div>
        </section>

        <!-- =========== Interactive Demo Section =========== -->
        <section id="demo" class="py-20">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Demo Interactiva</h2>
                    <p class="mt-4 text-gray-600">Experimenta el poder de EcoBuild. Interactúa con un modelo de Sugarcrete.</p>
                </div>
                <div class="bg-white rounded-xl shadow-2xl overflow-hidden">
                    <div class="w-full h-96 md:h-[500px] bg-gray-900" id="demo-canvas-container">
                        <!-- El canvas de Three.js se insertará aquí -->
                    </div>
                    <div class="p-6 text-center bg-gray-50">
                        <h3 class="text-xl font-bold">Edificio Sostenible "Amapola"</h3>
                        <p class="text-gray-600 mt-2">Este modelo fue generado con EcoBuild, optimizando la estructura con Sugarcrete para el clima local.</p>
                        <button class="mt-4 bg-gray-800 text-white font-semibold px-6 py-2 rounded-lg hover:bg-black transition-colors">
                            Activar Vista AR (Próximamente)
                        </button>
                    </div>
                </div>
            </div>
        </section>

        <!-- =========== Download Section =========== -->
        <section id="download" class="py-20 bg-emerald-600 text-white">
            <div class="container mx-auto px-6 text-center">
                <h2 class="text-3xl md:text-4xl font-bold">Empieza a Construir un Futuro Mejor Hoy</h2>
                <p class="mt-4 max-w-2xl mx-auto">Descarga EcoBuild en tu plataforma preferida o regístrate para usar la versión web.</p>
                <div class="mt-8 flex flex-wrap justify-center items-center gap-4">
                    <a href="#" class="bg-white text-emerald-700 font-semibold px-6 py-3 rounded-lg flex items-center space-x-2 hover:bg-gray-200 transition-all shadow-lg transform hover:-translate-y-1">
                        <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M12 20.94c1.5 0 2.75 1.06 4 1.06 3 0 6-8 6-12.22A4.91 4.91 0 0 0 17 5c-2.22 0-4 1.44-5 2-1-.56-2.78-2-5-2a4.9 4.9 0 0 0-5 4.78C2 14 5 22 8 22c1.25 0 2.5-1.06 4-1.06Z"/><path d="M10 2c1 .5 2 2 2 5"/></svg>
                        <span>App Store</span>
                    </a>
                    <a href="#" class="bg-white text-emerald-700 font-semibold px-6 py-3 rounded-lg flex items-center space-x-2 hover:bg-gray-200 transition-all shadow-lg transform hover:-translate-y-1">
                       <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><path d="M15.2 3.8a2 2 0 0 1 2.8.7l2.8 4.4a2 2 0 0 1 .1 1.6l-2.1 5.5a2 2 0 0 1-1.8 1.2H6.8a2 2 0 0 1-1.8-1.2L2.9 10.5a2 2 0 0 1 .1-1.6l2.8-4.4a2 2 0 0 1 2.8-.7z"/><path d="M6 17h12"/></svg>
                        <span>Google Play</span>
                    </a>
                    <a href="#" class="bg-white text-emerald-700 font-semibold px-6 py-3 rounded-lg flex items-center space-x-2 hover:bg-gray-200 transition-all shadow-lg transform hover:-translate-y-1">
                       <svg xmlns="http://www.w3.org/2000/svg" width="24" height="24" viewBox="0 0 24 24" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"><rect x="2" y="3" width="20" height="14" rx="2" ry="2"></rect><line x1="8" y1="21" x2="16" y2="21"></line><line x1="12" y1="17" x2="12" y2="21"></line></svg>
                        <span>Versión Escritorio</span>
                    </a>
                </div>
            </div>
        </section>

        <!-- =========== FAQ Section =========== -->
        <section id="faq" class="py-20">
            <div class="container mx-auto px-6 max-w-4xl">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Preguntas Frecuentes</h2>
                    <p class="mt-4 text-gray-600">Resolvemos tus dudas más comunes sobre EcoBuild.</p>
                </div>
                <div class="space-y-4">
                    <!-- FAQ Item -->
                    <div class="faq-item bg-white rounded-lg shadow-sm border border-gray-200">
                        <button class="question w-full flex justify-between items-center p-6 text-left">
                            <span class="text-lg font-semibold">¿Qué es Sugarcrete y por qué usarlo?</span>
                            <span class="icon-plus text-emerald-500"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4" /></svg></span>
                            <span class="icon-minus text-emerald-500"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 12H4" /></svg></span>
                        </button>
                        <div class="answer px-6 pb-6 text-gray-600">
                            Sugarcrete es un innovador material de construcción sostenible hecho a partir de bagazo de caña de azúcar, un subproducto de la industria azucarera. Es una alternativa al hormigón tradicional con una huella de carbono mucho menor, excelente resistencia y propiedades de aislamiento térmico.
                        </div>
                    </div>
                    <!-- FAQ Item -->
                    <div class="faq-item bg-white rounded-lg shadow-sm border border-gray-200">
                        <button class="question w-full flex justify-between items-center p-6 text-left">
                            <span class="text-lg font-semibold">¿EcoBuild se integra con otras herramientas como BIM?</span>
                            <span class="icon-plus text-emerald-500"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4" /></svg></span>
                            <span class="icon-minus text-emerald-500"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 12H4" /></svg></span>
                        </button>
                        <div class="answer px-6 pb-6 text-gray-600">
                           Sí, EcoBuild está diseñado para ser escalable e interoperable. Estamos desarrollando activamente integraciones y plugins para que puedas importar y exportar tus proyectos a los principales software de modelado de información de construcción (BIM) como Revit, ArchiCAD y otros.
                        </div>
                    </div>
                    <!-- FAQ Item -->
                    <div class="faq-item bg-white rounded-lg shadow-sm border border-gray-200">
                        <button class="question w-full flex justify-between items-center p-6 text-left">
                            <span class="text-lg font-semibold">¿Cómo protege EcoBuild mis datos y proyectos?</span>
                            <span class="icon-plus text-emerald-500"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M12 4v16m8-8H4" /></svg></span>
                            <span class="icon-minus text-emerald-500"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M20 12H4" /></svg></span>
                        </button>
                        <div class="answer px-6 pb-6 text-gray-600">
                            La seguridad es nuestra máxima prioridad. Utilizamos cifrado de extremo a extremo para todos los datos del proyecto, tanto en tránsito como en reposo. Nuestra infraestructura en la nube cumple con los más altos estándares de seguridad y seguimos todas las normativas de privacidad de datos, como el GDPR.
                        </div>
                    </div>
                </div>
            </div>
        </section>

         <!-- =========== Contact Section =========== -->
        <section id="contact" class="py-20 bg-gray-100">
            <div class="container mx-auto px-6">
                <div class="text-center mb-12">
                    <h2 class="text-3xl md:text-4xl font-bold text-gray-900">Contacto y Soporte</h2>
                    <p class="mt-4 text-gray-600">¿Tienes alguna pregunta o comentario? Nos encantaría escucharte.</p>
                </div>
                <div class="max-w-xl mx-auto bg-white p-8 rounded-lg shadow-lg">
                    <form id="contact-form">
                        <div class="mb-4">
                            <label for="name" class="block text-gray-700 font-semibold mb-2">Nombre</label>
                            <input type="text" id="name" name="name" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500">
                        </div>
                        <div class="mb-4">
                            <label for="email" class="block text-gray-700 font-semibold mb-2">Correo Electrónico</label>
                            <input type="email" id="email" name="email" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500">
                        </div>
                        <div class="mb-6">
                            <label for="message" class="block text-gray-700 font-semibold mb-2">Mensaje</label>
                            <textarea id="message" name="message" rows="4" required class="w-full px-4 py-2 border border-gray-300 rounded-lg focus:outline-none focus:ring-2 focus:ring-emerald-500"></textarea>
                        </div>
                        <button type="submit" class="w-full bg-emerald-500 text-white font-bold px-6 py-3 rounded-lg hover:bg-emerald-600 transition-all shadow-md">
                            Enviar Mensaje
                        </button>
                        <p id="form-status" class="text-center mt-4"></p>
                    </form>
                </div>
            </div>
        </section>
    </main>
    
    <!-- =========== Footer =========== -->
    <footer class="bg-gray-800 text-white">
        <div class="container mx-auto px-6 py-12">
            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div>
                    <h3 class="text-lg font-semibold mb-4">EcoBuild</h3>
                    <p class="text-gray-400">Diseñando un futuro sostenible, un proyecto a la vez.</p>
                </div>
                <div>
                    <h3 class="text-lg font-semibold mb-4">Comparte</h3>
                    <div class="flex space-x-4">
                        <a href="#" class="share-btn text-gray-400 hover:text-white" data-network="facebook" title="Compartir en Facebook"><svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M18 2h-3a5 5 0 00-5 5v3H7v4h3v8h4v-8h3l1-4h-4V7a1 1 0 011-1h3z"></path></svg></a>
                        <a href="#" class="share-btn text-gray-400 hover:text-white" data-network="twitter" title="Compartir en Twitter"><svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M23 3a10.9 10.9 0 01-3.14 1.53 4.48 4.48 0 00-7.86 3v1A10.66 10.66 0 013 4s-4 9 5 13a11.64 11.64 0 01-7 2c9 5 20 0 20-11.5a4.5 4.5 0 00-.08-.83A7.72 7.72 0 0023 3z"></path></svg></a>
                        <a href="#" class="share-btn text-gray-400 hover:text-white" data-network="linkedin" title="Compartir en LinkedIn"><svg class="w-6 h-6" fill="currentColor" viewBox="0 0 24 24"><path d="M16 8a6 6 0 016 6v7h-4v-7a2 2 0 00-2-2 2 2 0 00-2 2v7h-4v-7a6 6 0 016-6zM6 9H2v12h4zM4 6.47A2.5 2.5 0 016.5 4 2.5 2.5 0 019 6.47a2.5 2.5 0 01-5 0z"></path></svg></a>
                        <a href="#" class="share-btn text-gray-400 hover:text-white" data-network="email" title="Compartir por Correo"><svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg></a>
                    </div>
                </div>
            </div>
            <div class="mt-12 border-t border-gray-700 pt-8 text-center text-gray-400 text-sm">
                <p>&copy; <span id="year"></span> EcoBuild Inc. Todos los derechos reservados.</p>
                <p class="mt-2"><a href="#" class="hover:text-white">Política de Privacidad</a> | <a href="#" class="hover:text-white">Términos de Servicio</a></p>
            </div>
        </div>
    </footer>

    <script type="module">
        // Import Three.js
        import * as THREE from 'three';
        import { OrbitControls } from 'three/addons/controls/OrbitControls.js';

        // --- Demo 3D ---
        function init3D_Demo() {
            const container = document.getElementById('demo-canvas-container');
            if (!container) return;

            // Escena, Cámara, Renderizador
            const scene = new THREE.Scene();
            scene.background = new THREE.Color(0x111827); // bg-gray-900

            const camera = new THREE.PerspectiveCamera(75, container.clientWidth / container.clientHeight, 0.1, 1000);
            camera.position.z = 5;

            const renderer = new THREE.WebGLRenderer({ antialias: true });
            renderer.setSize(container.clientWidth, container.clientHeight);
            container.appendChild(renderer.domElement);

            // Controles Orbitales
            const controls = new OrbitControls(camera, renderer.domElement);
            controls.enableDamping = true;
            controls.autoRotate = true;
            controls.autoRotateSpeed = 0.5;

            // Luces
            const ambientLight = new THREE.AmbientLight(0xffffff, 0.5);
            scene.add(ambientLight);
            const pointLight = new THREE.PointLight(0xffffff, 0.8);
            pointLight.position.set(5, 5, 5);
            scene.add(pointLight);

            // Objeto (representando el edificio de Sugarcrete)
            const geometry = new THREE.BoxGeometry(2, 2, 2);
            const material = new THREE.MeshStandardMaterial({ 
                color: 0x10B981, // emerald-500
                roughness: 0.6,
                metalness: 0.2
            });
            const cube = new THREE.Mesh(geometry, material);
            scene.add(cube);

            // Loop de animación
            function animate() {
                requestAnimationFrame(animate);
                controls.update();
                renderer.render(scene, camera);
            }
            animate();
            
            // Responsividad del canvas
            window.addEventListener('resize', () => {
                camera.aspect = container.clientWidth / container.clientHeight;
                camera.updateProjectionMatrix();
                renderer.setSize(container.clientWidth, container.clientHeight);
            });
        }
        
        // --- Scripts de la página ---
        document.addEventListener('DOMContentLoaded', () => {
            init3D_Demo();
        
            // Menú móvil
            const mobileMenuButton = document.getElementById('mobile-menu-button');
            const mobileMenu = document.getElementById('mobile-menu');
            mobileMenuButton.addEventListener('click', () => {
                mobileMenu.classList.toggle('hidden');
            });
            
            // Cerrar menú al hacer clic en un enlace
            mobileMenu.addEventListener('click', (e) => {
                 if(e.target.tagName === 'A') {
                     mobileMenu.classList.add('hidden');
                 }
            });

            // FAQ Accordion
            const faqItems = document.querySelectorAll('.faq-item');
            faqItems.forEach(item => {
                const question = item.querySelector('.question');
                question.addEventListener('click', () => {
                    // Cierra otros items abiertos para un efecto de acordeón limpio
                    faqItems.forEach(otherItem => {
                        if (otherItem !== item) {
                            otherItem.classList.remove('open');
                        }
                    });
                    item.classList.toggle('open');
                });
            });

            // Formulario de contacto
            const contactForm = document.getElementById('contact-form');
            const formStatus = document.getElementById('form-status');
            contactForm.addEventListener('submit', (e) => {
                e.preventDefault();
                formStatus.textContent = 'Gracias por tu mensaje. Nos pondremos en contacto contigo pronto.';
                formStatus.className = 'text-center mt-4 text-emerald-600';
                contactForm.reset();
                setTimeout(() => formStatus.textContent = '', 3000);
            });
            
            // Botones de compartir
            const shareButtons = document.querySelectorAll('.share-btn');
            shareButtons.forEach(btn => {
                btn.addEventListener('click', (e) => {
                    e.preventDefault();
                    const network = btn.dataset.network;
                    const url = window.location.href;
                    const text = "Descubre EcoBuild: la plataforma para arquitectura sostenible con IA.";
                    let shareUrl = '';

                    switch(network) {
                        case 'facebook':
                            shareUrl = `https://www.facebook.com/sharer/sharer.php?u=${encodeURIComponent(url)}`;
                            break;
                        case 'twitter':
                            shareUrl = `https://twitter.com/intent/tweet?url=${encodeURIComponent(url)}&text=${encodeURIComponent(text)}`;
                            break;
                        case 'linkedin':
                            shareUrl = `https://www.linkedin.com/shareArticle?mini=true&url=${encodeURIComponent(url)}&title=EcoBuild&summary=${encodeURIComponent(text)}`;
                            break;
                        case 'email':
                            shareUrl = `mailto:?subject=Echa un vistazo a EcoBuild&body=${encodeURIComponent(text)}%0A%0A${encodeURIComponent(url)}`;
                            break;
                    }
                    if(shareUrl) {
                        window.open(shareUrl, '_blank', 'width=600,height=400');
                    }
                });
            });

            // Actualizar año en el footer
            document.getElementById('year').textContent = new Date().getFullYear();
        });
    </script>

</body>
</html>
