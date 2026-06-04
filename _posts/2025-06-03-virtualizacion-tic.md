---
title: Virtualización en TIC
layout: post
permalink: /virtualizacion-tic/
background: '#2c3e50'

slides:
 - title: Solución Estratificada
   slide-data: |
     <h2 style="color: #ecf0f1; font-size: 1.2em;">Problemas en TIC</h2>
     <hr style="border-color: #3498db; margin: 10px 0;">
     <p style="font-size: 0.9em; text-align: justify; line-height: 1.4;">
       La solución de problemas en Tecnologías de la Información y Comunicación se divide frecuentemente en diferentes niveles o capas (estratos).
     </p>
   theme: black

 - title: 1.1 Temas de Virtualización
   slide-data: |
     <ul style="font-size: 1.0em; line-height: 1.6; margin-top: 20px;">
       <li><strong>1.1.a</strong> Virtualización por interpretación pura</li>
       <li><strong>1.1.b</strong> Virtualización por recompilación dinámica</li>
       <li><strong>1.1.c</strong> Virtualización por hipervisión (bare metal)</li>
     </ul>
     <p style="margin-top: 30px; font-size: 0.8em; color: #bdc3c7;"><em>Cada método ofrece diferentes ventajas según el caso de uso</em></p>
   theme: black

 - title: 1.1.a - Interpretación Pura
   slide-data: |
     <h3 style="color: #34495e;">Descripción</h3>
     <p style="font-size: 0.9em; text-align: justify;">La máquina virtual interpreta cada instrucción del sistema huésped y la traduce al hardware real en tiempo de ejecución. No existe traducción previa o compilación.</p>
   background: '#34495e'

 - title: 1.1.a - Características
   slide-data: |
     <h3 style="color: #34495e;">Características principales</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li>Portabilidad máxima - puede ejecutar múltiples arquitecturas</li>
       <li>Simplicidad de implementación</li>
       <li>Bajo rendimiento debido a la interpretación continua</li>
       <li>Independencia del hardware subyacente</li>
       <li>Mayor consumo de recursos CPU</li>
     </ul>
   background: '#34495e'

 - title: 1.1.a - Casos de Uso
   slide-data: |
     <h3 style="color: #2980b9;">Casos de Uso</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li><strong>Emulación de sistemas antiguos:</strong> Ejecutar sistemas operativos heredados en hardware moderno</li>
       <li><strong>Cross-platform development:</strong> Desarrollar y probar software para diferentes arquitecturas</li>
       <li><strong>Educación:</strong> Aprendizaje sobre arquitecturas de computadores</li>
     </ul>
   background: '#2980b9'

 - title: 1.1.a - Ejemplos
   slide-data: |
     <h3 style="color: #2980b9;">Ejemplos</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li><strong>QEMU:</strong> Quick Emulator, múltiples arquitecturas</li>
       <li><strong>Bochs:</strong> Emulador x86 de código abierto</li>
       <li><strong>DOSBox:</strong> Emulador de DOS para juegos clásicos</li>
       <li><strong>MAME:</strong> Multiple Arcade Machine Emulator</li>
     </ul>
   background: '#2980b9'

 - title: 1.1.b - Recompilación Dinámica
   slide-data: |
     <h3 style="color: #8e44ad;">Descripción</h3>
     <p style="font-size: 0.9em; text-align: justify;">Las instrucciones del sistema huésped se traducen a código nativo durante la ejecución. El código traducido se cachea para reutilización, mejorando el rendimiento progresivamente.</p>
   background: '#8e44ad'

 - title: 1.1.b - Características
   slide-data: |
     <h3 style="color: #8e44ad;">Características principales</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li>Balance entre portabilidad y rendimiento</li>
       <li>Compilación JIT (Just-In-Time) de bloques de código</li>
       <li>Caché de código compilado para aceleración</li>
       <li>Hotspot detection para optimización de código crítico</li>
       <li>Mayor complejidad que interpretación pura</li>
     </ul>
   background: '#8e44ad'

 - title: 1.1.b - Casos de Uso
   slide-data: |
     <h3 style="color: #9b59b6;">Casos de Uso</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li><strong>Android emulators:</strong> Ejecución de apps Android en otros sistemas</li>
       <li><strong>Console emulation:</strong> Emulación eficiente de consolas de videojuegos</li>
       <li><strong>Cross-compilation testing:</strong> Pruebas en múltiples plataformas</li>
       <li><strong>Legacy migration:</strong> Migración de sistemas heredados</li>
     </ul>
   background: '#9b59b6'

 - title: 1.1.b - Ejemplos
   slide-data: |
     <h3 style="color: #9b59b6;">Ejemplos</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li><strong>QEMU con TCG:</strong> Tiny Code Generator</li>
       <li><strong>Android Emulator (AVD):</strong> Basado en QEMU con TCG</li>
       <li><strong>Dolphin Emulator:</strong> Wii/GameCube con recompilación JIT</li>
       <li><strong>RetroArch:</strong> Multi-emulador con recompilación</li>
     </ul>
   background: '#9b59b6'

 - title: 1.1.c - Hipervisión Bare Metal
   slide-data: |
     <h3 style="color: #c0392b;">Descripción</h3>
     <p style="font-size: 0.9em; text-align: justify;">El hipervisor se ejecuta directamente sobre el hardware físico (Tipo 1), sin necesidad de un sistema operativo huésped. Ofrece acceso directo al hardware y máximo rendimiento.</p>
   background: '#c0392b'

 - title: 1.1.c - Características
   slide-data: |
     <h3 style="color: #c0392b;">Características principales</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li>Máximo rendimiento y mínimo overhead</li>
       <li>Acceso directo al hardware físico</li>
       <li>Aislamiento completo entre máquinas virtuales</li>
       <li>Hardware-assisted virtualization (VT-x, AMD-V)</li>
       <li>Alta disponibilidad y características de cluster</li>
     </ul>
   background: '#c0392b'

 - title: 1.1.c - Casos de Uso
   slide-data: |
     <h3 style="color: #e74c3c;">Casos de Uso</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li><strong>Centros de datos:</strong> Consolidación de servidores empresariales</li>
       <li><strong>Cloud computing:</strong> Infraestructura como servicio (IaaS)</li>
       <li><strong>VPS hosting:</strong> Servidores virtuales privados</li>
       <li><strong>High availability:</strong> Clusters de alta disponibilidad</li>
       <li><strong>DevOps/Testing:</strong> Entornos aislados</li>
     </ul>
   background: '#e74c3c'

 - title: 1.1.c - Ejemplos
   slide-data: |
     <h3 style="color: #e74c3c;">Ejemplos</h3>
     <ul style="font-size: 0.9em; line-height: 1.5;">
       <li><strong>VMware ESXi:</strong> Hipervisor empresarial</li>
       <li><strong>Microsoft Hyper-V:</strong> Solución Microsoft</li>
       <li><strong>Citrix XenServer:</strong> Basado en Xen</li>
       <li><strong>KVM:</strong> Open-source para Linux</li>
     </ul>
   background: '#e74c3c'

 - title: Comparativa de Estrategias
   slide-data: |
     <table style="font-size: 0.7em; margin: 10px auto; border-collapse: collapse;">
       <tr style="background: #2c3e50; color: white;">
         <th style="padding: 10px; border: 1px solid #34495e;">Característica</th>
         <th style="padding: 10px; border: 1px solid #34495e;">Interpretación</th>
         <th style="padding: 10px; border: 1px solid #34495e;">Recompilación</th>
         <th style="padding: 10px; border: 1px solid #34495e;">Bare Metal</th>
       </tr>
       <tr style="background: #34495e; color: #ecf0f1;">
         <td style="padding: 8px; border: 1px solid #556b82;"><strong>Portabilidad</strong></td>
         <td style="padding: 8px; border: 1px solid #556b82;">Excelente ⭐⭐⭐</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Muy Buena ⭐⭐⭐</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Limitada ⭐</td>
       </tr>
       <tr style="background: #445566; color: #ecf0f1;">
         <td style="padding: 8px; border: 1px solid #556b82;"><strong>Rendimiento</strong></td>
         <td style="padding: 8px; border: 1px solid #556b82;">Bajo ⭐</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Medio-Alto ⭐⭐</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Excelente ⭐⭐⭐</td>
       </tr>
       <tr style="background: #34495e; color: #ecf0f1;">
         <td style="padding: 8px; border: 1px solid #556b82;"><strong>Complejidad</strong></td>
         <td style="padding: 8px; border: 1px solid #556b82;">Baja ⭐</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Media ⭐⭐</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Alta ⭐⭐⭐</td>
       </tr>
       <tr style="background: #445566; color: #ecf0f1;">
         <td style="padding: 8px; border: 1px solid #556b82;"><strong>Overhead</strong></td>
         <td style="padding: 8px; border: 1px solid #556b82;">Alto</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Medio</td>
         <td style="padding: 8px; border: 1px solid #556b82;">Mínimo</td>
       </tr>
     </table>
   background: '#1a252f'

 - title: Conclusiones y Futuro
   slide-data: |
     <h3 style="color: #2c3e50;">Puntos Clave</h3>
     <ul style="font-size: 0.8em; line-height: 1.5;">
       <li><strong>Interpretación pura:</strong> Ideal cuando la portabilidad es prioritaria</li>
       <li><strong>Recompilación dinámica:</strong> Balance entre portabilidad y rendimiento moderno</li>
       <li><strong>Hipervisión bare metal:</strong> Máxima eficiencia para producción</li>
     </ul>
     <hr style="margin: 15px 0; border-color: #bdc3c7;">
     <h3 style="color: #2c3e50;">Tendencias Futuras</h3>
     <ul style="font-size: 0.8em; line-height: 1.5;">
       <li>Híbridos que combinan múltiples estrategias</li>
       <li>Hardware-assisted virtualization cada vez más potente</li>
       <li>Container-based virtualization como complemento</li>
     </ul>
   theme: black
---

{% for slide in page.slides %}
<section data-background="{% if slide.image %}{{slide.image}}{% elsif slide.background %}{{slide.background}}{% else %}{{page.background}}{% endif %}">
        <h4 style="font-size: 0.8em; margin-bottom: 5px; line-height: 1.2; color: #bdc3c7;">{{slide.title}}</h4>
        {{ slide.slide-data }}
</section>
{% endfor %}