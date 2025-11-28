<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width,initial-scale=1.0">
<title>Campaña de Control de Plagas</title>

<style>
    :root {
        --azul: #1e6fd9;
        --azul-rey: #d2eaff;
        --verde: #1dbf73;
        --verde-claro: #c4ffe4;
        --fondo: #eefaff;
    }
    body {
        margin:0;
        background: var(--fondo);
        font-family: Arial;
        overflow:hidden;
    }

    /* Pantalla inicial */
    #inicio {
        position: fixed;
        inset:0;
        background: rgba(0,40,60,0.55);
        backdrop-filter: blur(6px);
        display:flex;
        flex-direction:column;
        align-items:center;
        justify-content:center;
        z-index:999;
        transition: opacity 1s ease;
    }
    #inicio h1 {
        color:white;
        font-size:40px;
        margin-bottom:20px;
    }
    #inicio button {
        padding:12px 30px;
        background: var(--verde);
        color:white;
        border:none;
        border-radius:10px;
        font-size:18px;
        cursor:pointer;
    }

    /* Menú */
    nav {
        background: var(--azul);
        padding: 12px;
        display:flex;
        justify-content:center;
        gap:10px;
    }
    nav button {
        background: var(--verde);
        color:white;
        padding:10px 18px;
        border:none;
        border-radius:7px;
        cursor:pointer;
        font-size:15px;
    }

    /* Pantallas */
    .pantalla {
        display:none;
        padding:25px;
        height: calc(100vh - 70px);
        overflow-y: auto;
        animation: fade .4s ease;
    }
    .visible {
        display:block;
    }
    @keyframes fade {from {opacity:0;} to {opacity:1;}}

    h2 { color: var(--azul); }

    /* Usuario */
    .card {
        background:white;
        padding:20px;
        border-radius:8px;
        box-shadow:0 2px 10px rgba(0,0,0,0.1);
        max-width:400px;
    }

    /* Quiz */
    .pregunta-box {
        background:white;
        padding:15px;
        margin-bottom:18px;
        border-radius:8px;
        border-left:5px solid var(--verde);
    }
    .opcion {
        background: var(--azul-claro);
        padding:10px;
        margin:6px 0;
        border-radius:6px;
        cursor:pointer;
    }
    .correcta { background: #b0ffc4 !important; }
    .incorrecta { background: #ffbbbb !important; }
</style>
</head>

<body>

<!-- Pantalla inicial -->
<div id="inicio">
    <h1>Campaña sobre el Control de Plagas</h1>
    <button onclick="entrar()">Entrar</button>
</div>

<!-- Menú -->
<nav>
    <button onclick="cambiar(1)">Inicio</button>
    <button onclick="cambiar(2)">Tipos</button>
    <button onclick="cambiar(3)">Prevención</button>
    <button onclick="cambiar(4)">Soluciones</button>
    <button onclick="cambiar(5)">Problemas</button>
    <button onclick="cambiar(6)">Usuario</button>
    <button onclick="cambiar(7)">Didáctica</button>
</nav>

<!-- 1. Inicio -->
<div class="pantalla visible" id="p1">
   <div style="padding:25px; font-family:Arial; line-height:1.6; color:#00334d;">
    
    <h2 style="color:#1e6fd9;">¿Qué son las plagas?</h2>
    <p>
        Las plagas son organismos —principalmente animales, insectos o microorganismos— que afectan negativamente 
        la salud humana, los cultivos, las construcciones o el ambiente. Se vuelven plaga cuando su población 
        crece de manera descontrolada y genera daños económicos, sanitarios o ecológicos.
    </p>

    <h2 style="color:#1e6fd9;">¿Cómo se producen las plagas?</h2>
    <p>
        Las plagas se producen cuando un organismo encuentra las condiciones ideales para reproducirse de forma 
        rápida. Esto suele ocurrir en ambientes donde hay:
    </p>
    <ul>
        <li>Acceso continuo a alimentos</li>
        <li>Agua disponible</li>
        <li>Falta de depredadores naturales</li>
        <li>Espacios descuidados o con basura</li>
        <li>Clima adecuado para su reproducción</li>
    </ul>

    <h2 style="color:#1e6fd9;">¿Por qué aparecen las plagas?</h2>
    <p>
        Las plagas aparecen principalmente por desequilibrios ecológicos provocados por los humanos. 
        La acumulación de basura, el almacenamiento incorrecto de alimentos, las fugas de agua y la falta 
        de mantenimiento en hogares o ciudades generan el escenario perfecto para que cientos de especies 
        sobrevivan y se multipliquen.
    </p>

    <h2 style="color:#1e6fd9;">¿Cuál es la plaga más común del mundo?</h2>
    <p>
        La plaga más abundante del mundo es <b>la cucaracha alemana (Blattella germanica)</b>.  
        Está presente en casi todos los países y se adapta increíblemente rápido.  
        Otras plagas extremadamente comunes son:
    </p>
    <ul>
        <li>Mosquitos (el animal más mortal del planeta)</li>
        <li>Hormigas</li>
        <li>Ratas y ratones</li>
        <li>Termitas</li>
    </ul>

    <h2 style="color:#1e6fd9;">¿A qué se debe la existencia de las plagas?</h2>
    <p>
        La existencia de plagas se debe a procesos naturales, pero su proliferación actual está profundamente 
        ligada a actividades humanas como:
    </p>
    <ul>
        <li>Urbanización sin control</li>
        <li>Contaminación ambiental</li>
        <li>Falta de saneamiento básico</li>
        <li>Comercio internacional (transporta especies a nuevos lugares)</li>
        <li>Cambio climático</li>
    </ul>
    <p>
        Estos factores alteran los ecosistemas y permiten que ciertos organismos encuentren recursos ilimitados 
        para reproducirse.
    </p>

    <h2 style="color:#1e6fd9;">¿Cómo inició todo históricamente?</h2>
    <p>
        La presencia de plagas existe desde que existen los seres vivos. Sin embargo, el concepto de “control de plagas” 
        comenzó a formalizarse hace miles de años.  
    </p>
    <p>
        Los primeros registros de plagas aparecen en tablillas mesopotámicas y egipcias (alrededor del 2500 a.C.), 
        donde se describen daños en cosechas causados por roedores y langostas.
    </p>

    <h2 style="color:#1e6fd9;">Primeras investigaciones sobre plagas</h2>
    <p>
        El primer investigador formal de las plagas fue <b>Aristóteles</b>, alrededor del año 350 a.C.  
        Él documentó por primera vez el comportamiento de insectos como:
    </p>
    <ul>
        <li>Abejas</li>
        <li>Termitas</li>
        <li>Saltamontes</li>
        <li>Escarabajos</li>
    </ul>
    <p>
        Aristóteles es considerado el <b>padre de la entomología</b>, la ciencia que estudia los insectos.
    </p>

    <h2 style="color:#1e6fd9;">¿Cómo evolucionó el control de plagas?</h2>
    <p>
        • En la Edad Media se usaban hierbas y humo para ahuyentar insectos. <br>
        • En el siglo XIX surgió la agricultura científica. <br>
        • En 1939 se extendió el uso del DDT (posteriormente prohibido). <br>
        • Hoy se utilizan métodos modernos como control biológico, ultrasonidos, geles selectivos y manejo integrado de plagas.
    </p>

</div>

</div>

<!-- 2. Tipos -->
<div class="pantalla" id="p2">
    <h2>Tipos de Plagas</h2>
   <div style="padding:25px; font-family:Arial; color:#00334d; line-height:1.7;">

    <h2 style="color:#1e6fd9;">Tipos de Plagas que Existen en el Mundo</h2>
    <p>
        En el planeta existen cientos de especies que, bajo ciertas condiciones, pueden convertirse en plagas. 
        Cada una afecta de manera distinta al ser humano, a los animales, a las plantas o a las estructuras. 
        Estas son las categorías más importantes y estudiadas globalmente.
    </p>

    <!-- Plagas de Insectos -->
    <h3 style="color:#1dbf73;">1. Plagas de Insectos</h3>
    <p>
        Son las más comunes del planeta. Representan más del 70% de todas las plagas registradas. 
        Se reproducen rápidamente, se adaptan al clima, y pueden transmitir enfermedades o dañar cultivos y construcciones.
    </p>
    <ul>
        <li><b>Mosquitos:</b> Considerados el animal más mortal del mundo. Transmiten dengue, zika, chikunguña, malaria y más.</li>
        <li><b>Cucarachas:</b> Una de las plagas más resistentes. Hay más de 4,000 especies.</li>
        <li><b>Termitas:</b> Conocidas como “come madera”. Causan daños millonarios en estructuras.</li>
        <li><b>Hormigas:</b> Especialmente las hormigas locas, de fuego y carpinteras.</li>
        <li><b>Pulgas:</b> Parasitan mascotas y transmiten bacterias.</li>
        <li><b>Chinches:</b> Infestan camas, hoteles y casas; muy difíciles de eliminar.</li>
        <li><b>Avispas:</b> Algunas especies invaden techos, áticos y maderas.</li>
        <li><b>Lepidópteros plaga:</b> Como el gusano cogollero y gusano de seda salvaje, devastan cultivos.</li>
    </ul>

    <!-- Plagas de Roedores -->
    <h3 style="color:#1dbf73;">2. Plagas de Roedores</h3>
    <p>
        Los roedores forman una de las plagas urbanas más peligrosas. Portan más de 35 enfermedades, 
        contaminan alimentos y destruyen infraestructura al roer cables y tuberías.
    </p>
    <ul>
        <li><b>Rata negra:</b> La más común en zonas urbanas.</li>
        <li><b>Rata noruega:</b> Grande, agresiva y destructiva.</li>
        <li><b>Ratón doméstico:</b> Muy pequeño y extremadamente escurridizo.</li>
    </ul>

    <!-- Plagas de Aves -->
    <h3 style="color:#1dbf73;">3. Plagas de Aves</h3>
    <p>
        Aunque las aves son esenciales para los ecosistemas, algunas especies pueden convertirse en plaga al invadir ciudades o estructuras.
    </p>
    <ul>
        <li><b>Palomas:</b> Llamadas “ratas con alas”. Corroen estructuras con su ácido excremento.</li>
        <li><b>Gorriones:</b> Pueden infestar techos y nidos en maquinaria.</li>
        <li><b>Estorninos:</b> Multitudes gigantes que contaminan y alteran ecosistemas.</li>
    </ul>

    <!-- Plagas Agrícolas -->
    <h3 style="color:#1dbf73;">4. Plagas Agrícolas</h3>
    <p>
        Afectan de forma directa las cosechas y los sistemas de producción alimentaria. Sin control, 
        pueden destruir miles de hectáreas en semanas.
    </p>
    <ul>
        <li><b>Langostas del desierto:</b> Capaces de formar nubes de miles de millones.</li>
        <li><b>Pulgones:</b> Chupan la savia y transmiten virus a las plantas.</li>
        <li><b>Mosca blanca:</b> Una de las plagas más difíciles para tomates y hortalizas.</li>
        <li><b>Minadores de hojas:</b> Devoran internamente las hojas creando túneles.</li>
        <li><b>Gorgojos:</b> Atacan granos almacenados.</li>
    </ul>

    <!-- Plagas Acuáticas -->
    <h3 style="color:#1dbf73;">5. Plagas Acuáticas</h3>
    <p>
        Son especies invasoras que afectan lagos, ríos y mares, dañando la biodiversidad.
    </p>
    <ul>
        <li><b>Mejillón cebra:</b> Se pega a cualquier superficie sumergida y colapsa tuberías.</li>
        <li><b>Carpa asiática:</b> Compite con especies nativas y destruye ecosistemas.</li>
        <li><b>Alga tóxica (marea roja):</b> Mortal para peces y peligrosa para humanos.</li>
    </ul>

    <!-- Plagas de Ácaros -->
    <h3 style="color:#1dbf73;">6. Plagas de Ácaros</h3>
    <p>
        Invisibles a simple vista, pero comunes en casas, colchones y cultivos.
    </p>
    <ul>
        <li><b>Ácaros del polvo:</b> Causan alergias severas.</li>
        <li><b>Ácaro rojo:</b> Ataca plantas ornamentales y huertos.</li>
        <li><b>Sarna (ácaro parasitario):</b> Afecta piel humana y animal.</li>
    </ul>

    <!-- Plagas de Hongos -->
    <h3 style="color:#1dbf73;">7. Plagas Fúngicas (Hongos)</h3>
    <p>
        Los hongos afectan principalmente a plantas, alimentos almacenados y madera.
    </p>
    <ul>
        <li><b>Moho negro:</b> Muy tóxico para la salud humana.</li>
        <li><b>Oídio:</b> Un hongo blanco que afecta frutas y verduras.</li>
        <li><b>Fusarium:</b> Mata plantas desde la raíz.</li>
        <li><b>Botrytis:</b> Hongo gris que destruye cosechas enteras.</li>
    </ul>

    <!-- Plagas de Bacterias -->
    <h3 style="color:#1dbf73;">8. Plagas Bacterianas</h3>
    <p>
        Son microorganismos que infectan plantas, animales o alimentos y causan enfermedades graves.
    </p>
    <ul>
        <li><b>Salmonella:</b> Contamina alimentos mal cocidos.</li>
        <li><b>Escherichia coli:</b> Proviene de agua contaminada.</li>
        <li><b>Xanthomonas:</b> Plaga bacteriana en cultivos tropicales.</li>
    </ul>

    <!-- Epílogo -->
    <h3 style="color:#1dbf73;">Conclusión</h3>
    <p>
        Las plagas afectan a todos los ecosistemas del mundo, desde hogares y ciudades hasta campos y océanos. 
        Conocerlas es el primer paso para prevenirlas y actuar de forma responsable. Su presencia está ligada 
        al desequilibrio ambiental, a los cambios climáticos y a las actividades humanas.
    </p>

</div>

</div>

<!-- 3. Prevención -->
<div class="pantalla" id="p3">
    <h2>Prevención</h2>
<section id="prevencion-plagas" style="font-family: Arial; padding: 40px; background: #e8fff1; border-radius: 10px;">
    <h2 style="color:#0a8f6a;">Prevención de Plagas</h2>
    <p>
        La prevención de plagas es el conjunto de estrategias, prácticas y medidas diseñadas para evitar
        que animales, insectos u organismos dañinos se establezcan en un entorno. La clave para controlar
        plagas no es eliminarlas cuando aparecen, sino impedir que se desarrollen desde el inicio.  
    </p>

    <h3 style="color:#0a8f6a;">¿Por qué es importante la prevención?</h3>
    <p>
        Las plagas pueden transmitir enfermedades, contaminar alimentos, dañar estructuras, destruir
        cultivos y afectar la economía local. Prevenirlas evita gastos mayores, protege la salud pública,
        mantiene un ambiente seguro y reduce la necesidad de utilizar químicos agresivos.
    </p>

    <h3 style="color:#0a8f6a;">Medidas fundamentales de prevención</h3>
    <ul>
        <li><strong>Higiene constante:</strong> Mantener áreas limpias elimina fuentes de alimento y refugio.</li>
        <li><strong>Sellado de entradas:</strong> Tapar huecos, grietas y rendijas para impedir el acceso.</li>
        <li><strong>Almacenamiento seguro:</strong> Guardar comida en recipientes cerrados y resistentes.</li>
        <li><strong>Eliminación correcta de basura:</strong> Usar botes herméticos, retirar desechos diariamente.</li>
        <li><strong>Control de humedad:</strong> Las fugas y zonas húmedas atraen insectos como cucarachas y mosquitos.</li>
        <li><strong>Mantenimiento estructural:</strong> Reparar techos, tuberías, paredes y ventilaciones.</li>
        <li><strong>Podado de vegetación:</strong> Árboles y arbustos ayudan a plagas a acercarse a los hogares.</li>
        <li><strong>Manejo de alimentos y desperdicios:</strong> No dejar restos expuestos, limpiar derrames.</li>
        <li><strong>Inspecciones periódicas:</strong> Revisar sótanos, áticos, bodegas y puntos críticos.</li>
        <li><strong>Uso moderado de repelentes y trampas:</strong> Para zonas donde el riesgo sea elevado.</li>
    </ul>

    <h3 style="color:#0a8f6a;">Métodos avanzados de prevención</h3>
    <p>
        Para ambientes industriales o zonas rurales, la prevención debe ser más especializada:
    </p>
    <ul>
        <li><strong>Manejo Integrado de Plagas (MIP):</strong> Combina prácticas biológicas, físicas y químicas.</li>
        <li><strong>Control biológico:</strong> Uso de depredadores naturales como aves, hongos o bacterias.</li>
        <li><strong>Monitoreo constante:</strong> Trampas de feromonas, sensores inteligentes y cámaras.</li>
        <li><strong>Barreras físicas:</strong> Mallas, filtros de aire, sistemas de exclusión profesional.</li>
        <li><strong>Capacitación del personal:</strong> Vital en empresas de alimentos, escuelas y hospitales.</li>
    </ul>

    <h3 style="color:#0a8f6a;">Errores comunes que favorecen las plagas</h3>
    <ul>
        <li>Acumular objetos viejos que sirven como refugio.</li>
        <li>Dejar platos con restos de comida durante la noche.</li>
        <li>No reparar fugas o humedad constante.</li>
        <li>No limpiar detrás de refrigeradores, hornos o muebles grandes.</li>
        <li>Usar químicos sin conocimiento, lo que hace más resistentes a ciertas especies.</li>
    </ul>

    <h3 style="color:#0a8f6a;">Recomendaciones para hogares</h3>
    <p>
        En zonas residenciales, pequeños hábitos pueden marcar una gran diferencia:
    </p>
    <ul>
        <li>Barrer y trapear regularmente.</li>
        <li>Evitar guardar cajas de cartón por mucho tiempo.</li>
        <li>Tapar desagües por las noches.</li>
        <li>Mantener alimentos para mascotas bien almacenados.</li>
        <li>Ventilar todos los espacios al menos 10 minutos al día.</li>
    </ul>

    <h3 style="color:#0a8f6a;">Recomendaciones para negocios</h3>
    <ul>
        <li>Implementar auditorías internas mensuales.</li>
        <li>Contratar servicios profesionales de control de plagas.</li>
        <li>Establecer zonas libres de comida y rutas de limpieza.</li>
        <li>Documentar reportes y detectar patrones.</li>
        <li>Dar mantenimiento constante a maquinaria industrial.</li>
    </ul>

    <h3 style="color:#0a8f6a;">Conclusión</h3>
    <p>
        La prevención de plagas es una responsabilidad compartida entre hogares, negocios y comunidades
        completas. Mantener la limpieza, vigilar el entorno y entender cómo actúan las plagas permite
        mantener su presencia bajo control. La prevención no es un gasto: es una inversión en salud,
        seguridad y bienestar.
    </p>
</section>

</div>

<!-- 4. Soluciones -->
<div class="pantalla" id="p4">
    <h2>Soluciones</h2>
<section id="soluciones-plagas" style="font-family: Arial; padding: 40px; background: #e6f9ff; border-radius: 12px;">
    <h2 style="color:#0083a3;">Soluciones para el Control de Plagas</h2>
    <p>
        Las soluciones para combatir plagas dependen del tipo de organismo, del lugar afectado y del nivel 
        de infestación. No existe una sola estrategia universal, pero sí un conjunto de métodos probados
        que, al combinarse, permiten erradicar, controlar y prevenir nuevos brotes de forma efectiva.
    </p>

    <h3 style="color:#0083a3;">1. Soluciones físicas</h3>
    <p>
        Son las técnicas que no requieren sustancias químicas. Se enfocan en eliminar la plaga mediante
        barreras, trampas o modificaciones del entorno.
    </p>
    <ul>
        <li><strong>Barreras físicas:</strong> Mallas mosquiteras, sellado de puertas, burletes, tapas herméticas.</li>
        <li><strong>Trampas mecánicas:</strong> Trampas adhesivas, trampas de luz UV, jaulas vivas para roedores.</li>
        <li><strong>Altas temperaturas:</strong> Vapor caliente para chinches, esterilización de ropa o muebles.</li>
        <li><strong>Bajas temperaturas:</strong> Congelación de alimentos infestados por polillas o gorgojos.</li>
        <li><strong>Aspirado y limpieza profunda:</strong> Eliminación de huevos, excremento y nidos.</li>
    </ul>

    <h3 style="color:#0083a3;">2. Soluciones químicas</h3>
    <p>
        Involucran el uso de sustancias diseñadas para eliminar o repeler plagas. Deben usarse con
        precaución y preferentemente por profesionales certificados.
    </p>
    <ul>
        <li><strong>Insecticidas residuales:</strong> Se aplican en grietas y paredes para eliminar insectos por contacto.</li>
        <li><strong>Fumigaciones:</strong> Gas o vapores para infestaciones fuertes como termitas o chinches.</li>
        <li><strong>Rodenticidas:</strong> Cebos para controlar ratas y ratones cuando las trampas no bastan.</li>
        <li><strong>Repelentes naturales:</strong> Aceites de citronela, eucalipto, neem o menta.</li>
        <li><strong>Reguladores de crecimiento:</strong> Evitan que insectos lleguen a etapa adulta.</li>
    </ul>

    <h3 style="color:#0083a3;">3. Soluciones biológicas</h3>
    <p>
        Se basa en el uso de organismos benéficos para combatir plagas sin dañar el ecosistema.
    </p>
    <ul>
        <li><strong>Depredadores naturales:</strong> Mariquitas contra pulgones, aves contra insectos voladores.</li>
        <li><strong>Hongos entomopatógenos:</strong> Especies que infectan y matan plagas específicas.</li>
        <li><strong>Bacterias beneficiosas:</strong> Como <em>Bacillus thuringiensis</em>, usada contra larvas de mosquitos.</li>
        <li><strong>Parásitos biológicos:</strong> Avispas diminutas que eliminan huevos de otros insectos.</li>
        <li><strong>Uso de feromonas:</strong> Para confundir a los machos e impedir la reproducción.</li>
    </ul>

    <h3 style="color:#0083a3;">4. Soluciones tecnológicas modernas</h3>
    <p>
        La ciencia actual ofrece herramientas innovadoras y de alta precisión.
    </p>
    <ul>
        <li><strong>Sensores inteligentes:</strong> Detectan movimiento, calor o feromonas en zonas críticas.</li>
        <li><strong>Trampas electrónicas:</strong> Para roedores o cucarachas con monitoreo remoto.</li>
        <li><strong>Ultrasonido:</strong> Dispositivos que emiten vibraciones molestan a roedores.</li>
        <li><strong>Drones agrícolas:</strong> Para detectar plagas en cultivos extensos.</li>
        <li><strong>Análisis de datos:</strong> Plataformas que predicen brotes mediante clima y geolocalización.</li>
    </ul>

    <h3 style="color:#0083a3;">5. Soluciones ecológicas y orgánicas</h3>
    <p>
        Son ideales para hogares, jardines, huertos urbanos y espacios donde no se desea usar químicos.
    </p>
    <ul>
        <li><strong>Vinagre blanco:</strong> Desinfectante y repelente suave contra hormigas.</li>
        <li><strong>Mezclas caseras:</strong> Jabón potásico, infusión de ajo, mezcla de limón con bicarbonato.</li>
        <li><strong>Plantas repelentes:</strong> Lavanda, romero, albahaca, menta.</li>
        <li><strong>Trampas caseras:</strong> Agua con jabón, vinagre de manzana, azúcar y levadura.</li>
        <li><strong>Control manual:</strong> Remover hojas dañadas, aplastar huevos, captar insectos.</li>
    </ul>

    <h3 style="color:#0083a3;">6. Manejo Integrado de Plagas (MIP)</h3>
    <p>
        Es el sistema más completo y eficiente, usado en agricultura, hospitales, restaurantes y zonas
        urbanas. Combina prevención, monitoreo y control equilibrado.
    </p>
    <ul>
        <li><strong>Identificación correcta:</strong> Saber qué plaga es para aplicar el método adecuado.</li>
        <li><strong>Monitoreo constante:</strong> Revisar puntos clave y registrar actividad.</li>
        <li><strong>Acción mínima necesaria:</strong> Empezar con métodos mecánicos antes de usar químicos.</li>
        <li><strong>Evaluación continua:</strong> Medir si las soluciones funcionaron y ajustarlas.</li>
        <li><strong>Educación y capacitación:</strong> Enseñar a las personas cómo prevenir nuevos brotes.</li>
    </ul>

    <h3 style="color:#0083a3;">7. ¿Qué solución elegir?</h3>
    <p>
        La solución ideal depende de:
    </p>
    <ul>
        <li>El nivel de infestación.</li>
        <li>El tipo de plaga.</li>
        <li>El entorno (hogar, empresa, campo abierto).</li>
        <li>La sensibilidad de las personas (alergias, mascotas, niños, alimentos expuestos).</li>
        <li>El impacto ambiental que se desea evitar.</li>
    </ul>

    <p>
        En casos leves, las soluciones físicas y ecológicas suelen ser suficientes.
        En casos moderados, se recomiendan soluciones combinadas.  
        En casos graves, lo mejor es contactar a un profesional para fumigación o manejo intensivo.
    </p>

    <h3 style="color:#0083a3;">Conclusión</h3>
    <p>
        Las plagas pueden parecer inevitables, pero con las soluciones adecuadas es posible reducir, controlar
        y erradicar su presencia. Lo más importante es actuar a tiempo, aplicar métodos seguros y mantener 
        una vigilancia constante para que la infestación no regrese.
    </p>
</section>

</div>

<!-- 5. Problemas -->
<div class="pantalla" id="p5">
    <h2>Problemas Causados</h2>
<section id="problemas-plagas" style="font-family: Arial; padding: 40px; background: #e9fff7; border-radius: 12px;">
    <h2 style="color:#0a8f6a;">Problemas Causados por las Plagas</h2>
    <p>
        Las plagas representan una de las mayores amenazas para la salud pública, la economía global, 
        la infraestructura, la agricultura y la estabilidad de los ecosistemas. Aunque algunos organismos 
        parecen inofensivos, cuando se reproducen sin control pueden provocar daños masivos y, en casos 
        extremos, situaciones de riesgo para toda una comunidad.  
    </p>

    <h3 style="color:#0a8f6a;">1. Problemas para la salud humana</h3>
    <p>
        Muchas plagas son transmisoras de enfermedades peligrosas. A través de mordeduras, picaduras, 
        excrementos, saliva o el simple contacto, pueden propagar virus, bacterias y parásitos.
    </p>
    <ul>
        <li><strong>Mosquitos:</strong> Transmiten dengue, zika, chikungunya, malaria y fiebre amarilla.</li>
        <li><strong>Ratas y ratones:</strong> Portadores de leptospirosis, hantavirus, rabia, salmonelosis.</li>
        <li><strong>Cucarachas:</strong> Propagan bacterias y empeoran el asma y alergias.</li>
        <li><strong>Pulgas y garrapatas:</strong> Causan enfermedad de Lyme, fiebre maculosa y peste bubónica.</li>
        <li><strong>Moscas:</strong> Contaminan alimentos con más de 200 tipos de microbios.</li>
    </ul>

    <h3 style="color:#0a8f6a;">2. Problemas en alimentos y salud pública</h3>
    <p>
        Las plagas pueden arruinar toneladas de alimentos en cuestión de semanas. Insectos, roedores y 
        microorganismos invaden bodegas, cocinas, fábricas y cultivos, haciendo que la comida ya no sea 
        apta para consumo humano.
    </p>
    <ul>
        <li><strong>Contaminación por excretas y saliva.</strong></li>
        <li><strong>Daño a empaques y envases.</strong></li>
        <li><strong>Retraso en cadenas de distribución.</strong></li>
        <li><strong>Pérdidas económicas enormes en agricultura y comercio.</strong></li>
        <li><strong>Brotes de enfermedades gastrointestinales.</strong></li>
    </ul>

    <h3 style="color:#0a8f6a;">3. Problemas estructurales</h3>
    <p>
        Muchas plagas no solo ensucian —destruyen. Algunas especies afectan directamente estructuras,
        maderas, cables, paredes y sistemas completos dentro de edificios, hogares y fábricas.
    </p>
    <ul>
        <li><strong>Termitas:</strong> Destrozan madera, vigas y estructuras enteras.</li>
        <li><strong>Roedores:</strong> Mastican cables eléctricos provocando cortos y riesgos de incendio.</li>
        <li><strong>Hormigas carpinteras:</strong> Debilitan paredes y estructuras internas.</li>
        <li><strong>Palomas:</strong> Corroen edificios con sus excrementos ácidos.</li>
        <li><strong>Murciélagos:</strong> Provocan deterioro por acumulación de guano.</li>
    </ul>

    <h3 style="color:#0a8f6a;">4. Problemas ambientales</h3>
    <p>
        Algunas plagas son consideradas invasoras: especies que llegan a un ecosistema donde no pertenecen
        y comienzan a desplazar a los animales nativos.
    </p>
    <ul>
        <li><strong>Competencia por alimento:</strong> Las especies invasoras consumen recursos esenciales.</li>
        <li><strong>Desbalance ecológico:</strong> Pueden alterar cadenas alimenticias completas.</li>
        <li><strong>Destrucción de hábitats:</strong> Roedores, insectos y aves en zonas naturales.</li>
        <li><strong>Extinción de especies locales:</strong> Por depredación o enfermedades traídas.</li>
        <li><strong>Contaminación del agua y suelo:</strong> A través de desechos y excretas.</li>
    </ul>

    <h3 style="color:#0a8f6a;">5. Problemas en agricultura y ganadería</h3>
    <p>
        Este es uno de los sectores más afectados por plagas en todo el mundo. Se estima que hasta 
        un 40% de los cultivos globales pueden perderse por plagas agrícolas si no se controlan.
    </p>
    <ul>
        <li><strong>Langostas:</strong> Pueden arrasar hectáreas de cultivos en horas.</li>
        <li><strong>Gusanos y larvas:</strong> Dañan raíces, hojas y frutos.</li>
        <li><strong>Hongos:</strong> Provocan pudriciones, mohos y enfermedades en plantas.</li>
        <li><strong>Ácaros:</strong> Degradan la calidad de frutas y hortalizas.</li>
        <li><strong>Parásitos del ganado:</strong> Causan debilidad, infección y baja producción.</li>
    </ul>

    <h3 style="color:#0a8f6a;">6. Problemas económicos</h3>
    <p>
        Las consecuencias económicas pueden ser devastadoras:
    </p>
    <ul>
        <li><strong>Pérdidas millonarias en insumos, alimentos y productos contaminados.</strong></li>
        <li><strong>Aumento en costos de fumigación y control profesional.</strong></li>
        <li><strong>Cierre temporal o permanente de negocios afectados.</strong></li>
        <li><strong>Interrupciones en importaciones y exportaciones.</strong></li>
        <li><strong>Incremento de precios en productos agrícolas.</strong></li>
    </ul>

    <h3 style="color:#0a8f6a;">7. Problemas emocionales y psicológicos</h3>
    <p>
        Vivir con plagas o tener una infestación severa puede generar efectos mentales importantes:
    </p>
    <ul>
        <li><strong>Ansiedad y estrés constante.</strong></li>
        <li><strong>Fobias a insectos o roedores.</strong></li>
        <li><strong>Problemas de sueño.</strong></li>
        <li><strong>Sensación de inseguridad en el hogar.</strong></li>
        <li><strong>Afectación en la autoestima del propietario.</strong></li>
    </ul>

    <h3 style="color:#0a8f6a;">8. Problemas en comercios e industrias</h3>
    <p>
        En negocios, una plaga puede arruinar la reputación de manera automática.
    </p>
    <ul>
        <li><strong>Multas y sanciones por salubridad.</strong></li>
        <li><strong>Pérdida de clientes inmediatos.</strong></li>
        <li><strong>Retiro de certificaciones sanitarias.</strong></li>
        <li><strong>Pérdida de inventario.</strong></li>
        <li><strong>Cierre de cadenas de distribución.</strong></li>
    </ul>

    <h3 style="color:#0a8f6a;">Conclusión</h3>
    <p>
        Las plagas no solo representan un inconveniente —son un problema grave con pérdidas humanas, 
        económicas, ecológicas y estructurales. Por eso el control, la prevención y la educación son 
        herramientas clave para enfrentar esta amenaza que afecta a todo el mundo.
    </p>
</section>

</div>

<!-- 6. Usuario / Base de Datos -->
<div class="pantalla" id="p6">
    <h2>Centro de Usuario</h2>
    <div class="card">
        <h3 id="estadoCuenta"></h3>

        <div id="login">
            <input id="user" type="text" placeholder="Nombre de usuario"><br><br>
            <input id="pass" type="password" placeholder="Contraseña"><br><br>
            <button onclick="registrar()">Registrar</button>
            <button onclick="iniciar()">Iniciar Sesión</button>
        </div>

        <div id="panelUsuario" style="display:none;">
            <p><b>Nombre actual:</b> <span id="nombreActual"></span></p>

            <label>Cambiar nombre:</label><br>
            <input id="nuevoNombre" type="text"><br><br>
            <button onclick="cambiarNombre()">Guardar cambio</button>
            <br><br>
            <p><b>Dato curioso:</b></p>
            <p id="datoCurioso"></p>

            <button onclick="cerrarSesion()" style="margin-top:20px;background:#ff6666;color:white;border:none;padding:10px 15px;border-radius:6px;">Cerrar Sesión</button>
        </div>
    </div>
</div>

<!-- 7. Didáctica -->
<div class="pantalla" id="p7">
    <h2>Preguntas Didácticas</h2>
    <div id="quiz"></div>
</div>


<script>
/* Cambiar pantallas */
function cambiar(n) {
    document.querySelectorAll(".pantalla").forEach(p => p.classList.remove("visible"));
    document.getElementById("p" + n).classList.add("visible");

    if (n === 6) cargarUsuario();
    if (n === 7) generarQuiz();
}

/* Pantalla entrada */
function entrar() {
    const p = document.getElementById("inicio");
    p.style.opacity = 0;
    setTimeout(()=>p.style.display="none",900);
}

/* Base de datos usuario */
function registrar() {
    let u = user.value.trim();
    let p = pass.value.trim();
    if (!u || !p) return alert("Completa todos los campos");

    localStorage.setItem("usuario", u);
    localStorage.setItem("clave", p);
    alert("Registrado correctamente");
}

function iniciar() {
    let u = user.value.trim();
    let p = pass.value.trim();
    if (u === localStorage.getItem("usuario") && p === localStorage.getItem("clave")) {
        localStorage.setItem("sesion", "activa");
        cargarUsuario();
    } else alert("Datos incorrectos");
}

function cargarUsuario() {
    let sesion = localStorage.getItem("sesion");
    if (sesion === "activa") {
        login.style.display = "none";
        panelUsuario.style.display = "block";
        nombreActual.textContent = localStorage.getItem("usuario");
        generarDato();
        estadoCuenta.textContent = "Sesión Iniciada";
    } else {
        login.style.display = "block";
        panelUsuario.style.display = "none";
        estadoCuenta.textContent = "Inicia sesión o regístrate";
    }
}

function cambiarNombre() {
    let nuevo = nuevoNombre.value.trim();
    if (!nuevo) return;
    localStorage.setItem("usuario", nuevo);
    nombreActual.textContent = nuevo;
    nuevoNombre.value = "";
    alert("Nombre actualizado");
}

function cerrarSesion() {
    localStorage.removeItem("sesion");
    cargarUsuario();
}

/* Datos curiosos */
const datos = [
    "Las cucarachas pueden vivir sin cabeza varios días.",
    "Los mosquitos son responsables de más de 700 mil muertes al año.",
    "Las ratas pueden saltar hasta 80 cm de altura.",
    "Las termitas nunca duermen.",
    "Las hormigas pueden cargar hasta 50 veces su propio peso."
];

function generarDato() {
    datoCurioso.textContent = datos[Math.floor(Math.random()*datos.length)];
}

/* Quiz con respuestas múltiples */
const preguntas = [
    {
        p: "¿Qué plaga transmite el dengue?",
        opciones: ["Mosquito", "Araña", "Hormiga"],
        correcta: 0
    },
    {
        p: "¿Qué insecto suele aparecer en lugares húmedos?",
        opciones: ["Cucaracha", "Avispa", "Mariposa"],
        correcta: 0
    },
    {
        p: "¿Qué plaga infesta la madera?",
        opciones: ["Termitas", "Mosquitos", "Ciempiés"],
        correcta: 0
    },
    {
        p: "¿Qué animal roe cables?",
        opciones: ["Ratón", "Gato", "Paloma"],
        correcta: 0
    },
    {
        p: "¿Qué evita la aparición de mosquitos?",
        opciones: ["Eliminar agua", "Apagar luces", "Cerrar ventanas"],
        correcta: 0
    }
];

function generarQuiz() {
    quiz.innerHTML = "";
    preguntas.forEach((q,i)=>{
        let box = document.createElement("div");
        box.className = "pregunta-box";
        box.innerHTML = <b>${q.p}</b>;

        q.opciones.forEach((op,idx)=>{
            let o = document.createElement("div");
            o.className = "opcion";
            o.textContent = op;
            o.onclick = ()=>seleccionar(o, idx === q.correcta);
            box.appendChild(o);
        });

        quiz.appendChild(box);
    });
}

function seleccionar(elem, correcto) {
    if (correcto) elem.classList.add("correcta");
    else elem.classList.add("incorrecta");
}
</script>
<!-- BOLITA FLOTANTE -->
<div id="chatBubble" style="
    width: 60px;
    height: 60px;
    background: #064f2d; 
    border-radius: 50%;
    position: fixed;
    bottom: 20px;
    right: 20px;
    cursor: pointer;
    z-index: 99999;
    display: flex;
    justify-content: center;
    align-items: center;
    color: white;
    font-size: 26px;
    box-shadow: 0 0 10px rgba(0,0,0,0.3);
">
💬
</div>

<!-- CHAT PEQUEÑO EN LA MISMA PÁGINA -->
<div id="stackChat" style="
    position: fixed;
    bottom: 90px;
    right: 20px;
    width: 320px;
    height: 420px;
    background: white;
    border-radius: 12px;
    box-shadow: 0 0 15px rgba(0,0,0,0.25);
    display: none;
    z-index: 99998;
    overflow: hidden;
">
    <!-- Cambia el src por el iframe DE TU CHAT -->
    <iframe src="https://www.stack-ai.com/chat/6927a7c575ad587df303ab64-1RYgDtVdvsnnZtV1KO48My"
        style="width:100%; height:100%; border:none;">
    </iframe>
</div>

<script>
  const bubble = document.getElementById("chatBubble");
  const chatWindow = document.getElementById("stackChat");
  let chatOpen = false;

  // ABRIR / CERRAR CHAT
  bubble.addEventListener("click", () => {
    chatOpen = !chatOpen;
    chatWindow.style.display = chatOpen ? "block" : "none";
  });

  // HACER LA BOLITA MOVIBLE
  let isDown = false;
  let offset = [0, 0];

  bubble.addEventListener('mousedown', function(e) {
      isDown = true;
      offset = [
          bubble.offsetLeft - e.clientX,
          bubble.offsetTop - e.clientY
      ];
      bubble.style.cursor = "grabbing";
  });

  document.addEventListener('mouseup', function() {
      isDown = false;
      bubble.style.cursor = "grab";
  });

  document.addEventListener('mousemove', function(e) {
      if (isDown) {
          bubble.style.left = (e.clientX + offset[0]) + 'px';
          bubble.style.top = (e.clientY + offset[1]) + 'px';
      }
  });
</script>

</body>
</html>
