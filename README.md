<!DOCTYPE html>
<html lang="es" class="scroll-smooth">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>CV Interactivo | Ana María Ochoa Patiño</title>
    <script src="https://cdn.tailwindcss.com"></script>
    <script src="https://cdn.jsdelivr.net/npm/chart.js"></script>
    <link rel="preconnect" href="https://fonts.googleapis.com">
    <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
    <link href="https://fonts.googleapis.com/css2?family=Inter:wght@400;500;600;700&display=swap" rel="stylesheet">
    <!-- Chosen Palette: Warm Neutrals (Background: #fdfaf6, Primary Text: #383838, Accent: #b88b4a, Secondary: #6b7280) -->
    <!-- Application Structure Plan: The SPA is designed thematically to guide the user from high-level impact to detailed evidence. 1) Hero: Immediate value proposition. 2) Impact Dashboard: Quantifiable achievements via KPI cards and an interactive chart to grab attention. 3) Case Studies: Filterable portfolio to explore specific projects, demonstrating problem-solving skills. 4) Competencies: Interactive radar chart to visualize skill distribution across key leadership domains. 5) Career Timeline: Chronological context for those who need it. This structure allows a recruiter to quickly grasp the candidate's value and then dive deep, which is more effective than a linear CV. -->
    <!-- Visualization & Content Choices: 1) Impact Dashboard (Goal: Show immediate value) -> KPI Cards + Bar Chart (Chart.js) for easy comparison of large-scale achievements. 2) Case Studies (Goal: Detail experience) -> Filterable HTML grid with modals to avoid clutter. 3) Competencies (Goal: Showcase skill balance) -> Radar Chart (Chart.js) is ideal for multi-axis comparison of leadership skills. 4) Timeline (Goal: Provide context) -> Styled HTML/CSS for a clean, readable chronological view. These choices prioritize interactivity and data clarity. -->
    <!-- CONFIRMATION: NO SVG graphics used. NO Mermaid JS used. -->
    <style>
        body {
            font-family: 'Inter', sans-serif;
            background-color: #fdfaf6;
            color: #383838;
        }
        .chart-container {
            position: relative;
            width: 100%;
            max-width: 800px;
            margin-left: auto;
            margin-right: auto;
            height: 350px;
            max-height: 400px;
        }
        @media (min-width: 768px) {
            .chart-container {
                height: 400px;
            }
        }
        .kpi-card {
            background-color: white;
            border-left: 5px solid #b88b4a;
            transition: transform 0.3s ease, box-shadow 0.3s ease;
        }
        .kpi-card:hover {
            transform: translateY(-5px);
            box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
        }
        .timeline-item::before {
            content: '';
            position: absolute;
            left: -30px;
            top: 0;
            width: 20px;
            height: 20px;
            border-radius: 50%;
            background-color: #b88b4a;
            border: 3px solid #fdfaf6;
        }
        .modal-overlay {
            transition: opacity 0.3s ease;
        }
        .modal-content {
            transition: transform 0.3s ease;
        }
    </style>
</head>
<body class="antialiased">

    <header id="home" class="sticky top-0 z-40 bg-[#fdfaf6]/80 backdrop-blur-lg border-b border-gray-200/50">
        <nav class="container mx-auto px-6 py-3 flex justify-between items-center">
            <h1 class="text-xl font-bold text-[#b88b4a]">Ana María Ochoa Patiño</h1>
            <div class="hidden md:flex space-x-8">
                <a href="#impact" class="text-gray-600 hover:text-[#b88b4a] transition-colors">Impacto</a>
                <a href="#portfolio" class="text-gray-600 hover:text-[#b88b4a] transition-colors">Casos de Estudio</a>
                <a href="#skills" class="text-gray-600 hover:text-[#b88b4a] transition-colors">Competencias</a>
                <a href="#career" class="text-gray-600 hover:text-[#b88b4a] transition-colors">Trayectoria</a>
            </div>
            <a href="mailto:8a.anamaria@gmail.com" class="hidden md:block bg-[#b88b4a] text-white px-4 py-2 rounded-md hover:bg-opacity-90 transition-colors">Contactar</a>
        </nav>
    </header>

    <main class="container mx-auto px-6">
        <section class="text-center py-20 md:py-32">
            <img src="https://placehold.co/128x128/e2e8f0/383838?text=AMO" alt="Ana María Ochoa Patiño" class="w-32 h-32 rounded-full mx-auto mb-6 ring-4 ring-[#b88b4a]/50">
            <h2 class="text-4xl md:text-5xl font-extrabold mb-4 leading-tight">Líder de Producto y Transformación Digital</h2>
            <p class="text-lg md:text-xl text-gray-600 max-w-3xl mx-auto">Conectando estrategia de negocio con ejecución técnica para entregar productos de alto impacto y fomentar culturas de innovación ágil.</p>
        </section>

        <section id="impact" class="py-16">
            <div class="text-center mb-12">
                <h3 class="text-3xl font-bold mb-2">Impacto Cuantificado</h3>
                <p class="text-gray-600 max-w-2xl mx-auto">Resultados medibles que demuestran la generación de valor a través del liderazgo estratégico y la gestión eficiente.</p>
            </div>
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-6 mb-12">
                <div class="kpi-card p-6 rounded-lg shadow-md">
                    <h4 class="text-3xl font-bold text-[#b88b4a]">$3.000M</h4>
                    <p class="text-gray-600">COP en portafolio de proyectos gestionado</p>
                </div>
                <div class="kpi-card p-6 rounded-lg shadow-md">
                    <h4 class="text-3xl font-bold text-[#b88b4a]">+200</h4>
                    <p class="text-gray-600">Colaboradores capacitados en metodologías ágiles</p>
                </div>
                <div class="kpi-card p-6 rounded-lg shadow-md">
                    <h4 class="text-3xl font-bold text-[#b88b4a]">-40%</h4>
                    <p class="text-gray-600">En bugs reportados en producción</p>
                </div>
                 <div class="kpi-card p-6 rounded-lg shadow-md">
                    <h4 class="text-3xl font-bold text-[#b88b4a]">+35 pts</h4>
                    <p class="text-gray-600">De incremento en NPS interno (50 a 85)</p>
                </div>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-lg">
                 <div class="chart-container">
                    <canvas id="impactChart"></canvas>
                </div>
            </div>
        </section>

        <section id="portfolio" class="py-16">
            <div class="text-center mb-12">
                <h3 class="text-3xl font-bold mb-2">Casos de Estudio</h3>
                <p class="text-gray-600 max-w-2xl mx-auto">Proyectos clave donde la aplicación de metodologías ágiles, la gestión de producto y el liderazgo estratégico generaron resultados tangibles.</p>
            </div>
            <div id="portfolio-grid" class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8">
            </div>
        </section>

        <section id="skills" class="py-16">
            <div class="text-center mb-12">
                <h3 class="text-3xl font-bold mb-2">Competencias Estratégicas</h3>
                <p class="text-gray-600 max-w-2xl mx-auto">Una visión 360° de mis habilidades, combinando la gestión de producto con el liderazgo ágil y la visión de negocio.</p>
            </div>
            <div class="bg-white p-6 rounded-xl shadow-lg">
                <div class="chart-container">
                    <canvas id="skillsRadarChart"></canvas>
                </div>
            </div>
        </section>

        <section id="career" class="py-16">
            <div class="text-center mb-12">
                <h3 class="text-3xl font-bold mb-2">Trayectoria Profesional y Académica</h3>
                <p class="text-gray-600 max-w-2xl mx-auto">Un recorrido por mi experiencia, desde la formación técnica hasta roles de liderazgo en transformación digital.</p>
            </div>
            <div class="relative max-w-2xl mx-auto border-l-2 border-gray-200 pl-8">
                 <div class="timeline-item mb-12">
                    <h4 class="font-bold text-lg text-[#b88b4a]">Consultora Senior de Transformación Digital</h4>
                    <p class="font-semibold">Grupo GTA | 2024 - Actualidad</p>
                    <p class="text-sm text-gray-500 mt-1">Diseño de PETI, arquitectura de soluciones SAP S/4HANA y gestión de proyectos de alta complejidad para expansión multinacional.</p>
                </div>
                <div class="timeline-item mb-12">
                    <h4 class="font-bold text-lg text-[#b88b4a]">Directora de Proyectos</h4>
                    <p class="font-semibold">Syspotec | 2023 - 2025</p>
                    <p class="text-sm text-gray-500 mt-1">Liderazgo de 6 equipos en la entrega de 25+ soluciones de software, optimizando calidad y gestionando un portafolio de $3.000M COP.</p>
                </div>
                <div class="timeline-item mb-12">
                    <h4 class="font-bold text-lg text-[#b88b4a]">Líder de Transformación Digital</h4>
                    <p class="font-semibold">AIR-E Sector Energético | 2020 - 2022</p>
                    <p class="text-sm text-gray-500 mt-1">Impulso de la cultura ágil, capacitando a +200 colaboradores y desarrollando un programa de gobierno de datos con Power BI.</p>
                </div>
                <div class="timeline-item mb-12">
                    <h4 class="font-bold text-lg text-[#b88b4a]">Product Owner</h4>
                    <p class="font-semibold">Digita Studio | 2022</p>
                    <p class="text-sm text-gray-500 mt-1">Concepción, desarrollo y definición del roadmap para un producto SaaS con operaciones en 4 países de Latinoamérica.</p>
                </div>
                <div class="timeline-item mb-12">
                    <h4 class="font-bold text-lg text-[#b88b4a]">Especialista en Evaluación de Proyectos</h4>
                    <p class="font-semibold">Universidad de Antioquia | 2018 - 2019</p>
                </div>
                 <div class="timeline-item">
                    <h4 class="font-bold text-lg text-[#b88b4a]">Ingeniera de Telecomunicaciones</h4>
                    <p class="font-semibold">Universidad Santo Tomás | 2010 - 2014</p>
                </div>
            </div>
        </section>
    </main>

    <footer class="bg-white mt-16 border-t">
        <div class="container mx-auto px-6 py-8 text-center text-gray-600">
            <p class="font-bold text-lg mb-2">¿Construimos algo increíble juntos?</p>
            <p>Estoy disponible para nuevos desafíos y colaboraciones.</p>
            <a href="mailto:8a.anamaria@gmail.com" class="inline-block mt-4 bg-[#b88b4a] text-white px-6 py-3 rounded-md hover:bg-opacity-90 transition-colors">Envíame un correo</a>
             <div class="mt-6">
                <a href="https://linkedin.com/in/8aanamaria" target="_blank" rel="noopener noreferrer" class="text-gray-500 hover:text-[#b88b4a]">LinkedIn</a>
            </div>
        </div>
    </footer>

    <div id="modal" class="modal-overlay fixed inset-0 bg-black bg-opacity-50 flex items-center justify-center p-4 z-50 opacity-0 pointer-events-none">
        <div id="modal-content" class="modal-content bg-white rounded-lg shadow-xl w-full max-w-2xl max-h-[90vh] overflow-y-auto p-8 transform scale-95">
            <div class="flex justify-between items-center border-b pb-3 mb-4">
                <h3 id="modal-title" class="text-2xl font-bold"></h3>
                <button id="close-modal-btn" class="text-gray-500 hover:text-gray-800 text-3xl leading-none">&times;</button>
            </div>
            <div id="modal-body">
            </div>
        </div>
    </div>

    <script>
        document.addEventListener('DOMContentLoaded', () => {

            const caseStudiesData = [
                {
                    id: 'gta',
                    title: 'Estrategia de Transformación Digital',
                    company: 'Grupo GTA',
                    tags: ['Estrategia', 'SAP', 'Agile Coach'],
                    problem: 'Un cliente multinacional requería una reestructuración estratégica de su tecnología para soportar la expansión, careciendo de una hoja de ruta clara y un ERP robusto.',
                    actions: [
                        'Diseño de un Plan Estratégico de Tecnología (PETI) que identificó y calificó 15 nuevas iniciativas de negocio.',
                        'Dirección de las decisiones de arquitectura para la implementación de SAP S/4HANA, asegurando la escalabilidad en tres países.',
                        'Implementación de un modelo de gobernanza ágil para equipos remotos.'
                    ],
                    results: [
                        'Incremento del 30% en la adopción de nuevas prácticas y eficiencia operativa.',
                        'Creación de una hoja de ruta cuantificable para la expansión de servicios.',
                        'Construcción de un pipeline de futuras oportunidades comerciales.'
                    ]
                },
                {
                    id: 'syspotec',
                    title: 'Gestión de Portafolio de Software',
                    company: 'Syspotec',
                    tags: ['Product Owner', 'Project Manager', 'KPIs'],
                    problem: 'Un portafolio de clientes clave del sector utilities experimentaba altos costos de soporte y baja satisfacción del cliente debido a un alto volumen de bugs.',
                    actions: [
                        'Liderazgo de 6 equipos multifuncionales (30 personas) en la entrega de 25 soluciones de software.',
                        'Establecimiento y monitoreo de KPIs de calidad del producto en dashboards de Power BI.',
                        'Administración de un portafolio de proyectos con un presupuesto total de $3.000M COP.'
                    ],
                    results: [
                        'Reducción del 40% en bugs reportados en producción en 12 meses.',
                        'Disminución del 25% en costos asociados a soporte.',
                        'Aumento significativo en los índices de satisfacción del cliente.'
                    ]
                },
                {
                    id: 'aire',
                    title: 'Adopción de Cultura Ágil',
                    company: 'AIR-E Sector Energético',
                    tags: ['Agile Coach', 'Cultura', 'Gobierno de Datos'],
                    problem: 'La organización necesitaba reducir el time-to-market y aumentar su capacidad de adaptación a los cambios del negocio, enfrentando una cultura tradicional.',
                    actions: [
                        'Capacitación a más de 200 colaboradores en Scrum y Kanban.',
                        'Desarrollo de un programa de "Data Champions" y centralización de indicadores en Power BI bajo la norma ISO 8000.',
                        'Impulso de 3 proyectos estratégicos basados en el feedback de los equipos.'
                    ],
                    results: [
                        'Aumento de la satisfacción interna (NPS) de 50 a 85/100.',
                        'Reducción del time-to-market de nuevas funcionalidades.',
                        'Establecimiento de un gobierno de datos robusto y centralizado.'
                    ]
                },
                {
                    id: 'digita',
                    title: 'Desarrollo de Producto SaaS',
                    company: 'Digita Studio (StartUp)',
                    tags: ['Product Owner', 'Roadmap', 'Arquitectura'],
                    problem: 'Una startup necesitaba concebir, desarrollar y lanzar un producto SaaS escalable que cumpliera con las regulaciones operativas de 4 países.',
                    actions: [
                        'Definición de la hoja de ruta (roadmap) completa del producto.',
                        'Supervisión de las decisiones de arquitectura para asegurar una plataforma escalable y adaptable.',
                        'Aplicación de técnicas de priorización (MoSCoW, RICE) para maximizar el ROI del desarrollo.'
                    ],
                    results: [
                        'El 90% de las entregas de valor se realizaron dentro de los timebox planificados.',
                        'Lanzamiento exitoso de una plataforma SaaS escalable y multi-país.',
                        'Maximización del retorno de inversión del ciclo de desarrollo.'
                    ]
                }
            ];

            const portfolioGrid = document.getElementById('portfolio-grid');
            caseStudiesData.forEach(study => {
                const card = document.createElement('div');
                card.className = 'bg-white rounded-lg shadow-md p-6 flex flex-col hover:shadow-xl transition-shadow duration-300 cursor-pointer';
                card.innerHTML = `
                    <h4 class="text-xl font-bold mb-2">${study.title}</h4>
                    <p class="text-gray-500 mb-4">${study.company}</p>
                    <div class="flex-grow">
                        <p class="text-gray-600">${study.problem}</p>
                    </div>
                    <div class="mt-4 flex flex-wrap gap-2">
                        ${study.tags.map(tag => `<span class="bg-gray-100 text-gray-600 text-xs font-semibold px-2.5 py-0.5 rounded-full">${tag}</span>`).join('')}
                    </div>
                `;
                card.addEventListener('click', () => openModal(study));
                portfolioGrid.appendChild(card);
            });

            const modal = document.getElementById('modal');
            const modalContent = document.getElementById('modal-content');
            const modalTitle = document.getElementById('modal-title');
            const modalBody = document.getElementById('modal-body');
            const closeModalBtn = document.getElementById('close-modal-btn');

            function openModal(study) {
                modalTitle.textContent = study.title;
                modalBody.innerHTML = `
                    <p class="text-gray-600 mb-6">${study.problem}</p>
                    <div class="grid grid-cols-1 md:grid-cols-2 gap-6">
                        <div>
                            <h5 class="font-bold text-lg mb-2 text-[#b88b4a]">Acciones Clave</h5>
                            <ul class="list-disc list-inside text-gray-600 space-y-2">
                                ${study.actions.map(action => `<li>${action}</li>`).join('')}
                            </ul>
                        </div>
                        <div>
                            <h5 class="font-bold text-lg mb-2 text-[#b88b4a]">Resultados</h5>
                            <ul class="list-disc list-inside text-gray-600 space-y-2">
                                ${study.results.map(result => `<li>${result}</li>`).join('')}
                            </ul>
                        </div>
                    </div>
                `;
                modal.classList.remove('opacity-0', 'pointer-events-none');
                modalContent.classList.remove('scale-95');
            }

            function closeModal() {
                modal.classList.add('opacity-0', 'pointer-events-none');
                modalContent.classList.add('scale-95');
            }

            closeModalBtn.addEventListener('click', closeModal);
            modal.addEventListener('click', (e) => {
                if (e.target === modal) {
                    closeModal();
                }
            });

            const impactCtx = document.getElementById('impactChart').getContext('2d');
            new Chart(impactCtx, {
                type: 'bar',
                data: {
                    labels: ['Presupuesto Gestionado (M COP)', 'Colaboradores Capacitados', 'Reducción de Bugs (%)', 'Incremento NPS (pts)'],
                    datasets: [{
                        label: 'Impacto Cuantificado',
                        data: [3000, 200, 40, 35],
                        backgroundColor: [
                            'rgba(184, 139, 74, 0.2)',
                            'rgba(184, 139, 74, 0.4)',
                            'rgba(184, 139, 74, 0.6)',
                            'rgba(184, 139, 74, 0.8)'
                        ],
                        borderColor: 'rgba(184, 139, 74, 1)',
                        borderWidth: 1
                    }]
                },
                options: {
                    indexAxis: 'y',
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                            display: false
                        },
                        tooltip: {
                            callbacks: {
                                label: function(context) {
                                    let label = context.dataset.label || '';
                                    if (label) {
                                        label += ': ';
                                    }
                                    if (context.parsed.x !== null) {
                                        label += context.parsed.x;
                                    }
                                    return label;
                                }
                            }
                        }
                    },
                    scales: {
                        x: {
                            beginAtZero: true,
                             ticks: {
                                callback: function(value, index, values) {
                                    if (value >= 1000) return value / 1000 + 'K';
                                    return value;
                                }
                            }
                        }
                    }
                }
            });

            const skillsCtx = document.getElementById('skillsRadarChart').getContext('2d');
            new Chart(skillsCtx, {
                type: 'radar',
                data: {
                    labels: ['Gestión de Producto', 'Liderazgo Ágil', 'Estrategia y Negocio', 'Análisis y Datos', 'Habilidades Técnicas'],
                    datasets: [{
                        label: 'Nivel de Competencia',
                        data: [9, 9, 8, 7, 6],
                        backgroundColor: 'rgba(184, 139, 74, 0.2)',
                        borderColor: 'rgba(184, 139, 74, 1)',
                        pointBackgroundColor: 'rgba(184, 139, 74, 1)',
                        pointBorderColor: '#fff',
                        pointHoverBackgroundColor: '#fff',
                        pointHoverBorderColor: 'rgba(184, 139, 74, 1)'
                    }]
                },
                options: {
                    responsive: true,
                    maintainAspectRatio: false,
                    plugins: {
                        legend: {
                           display: false
                        }
                    },
                    scales: {
                        r: {
                            angleLines: {
                                color: 'rgba(0, 0, 0, 0.1)'
                            },
                            grid: {
                                color: 'rgba(0, 0, 0, 0.1)'
                            },
                            pointLabels: {
                                font: {
                                    size: 14
                                },
                                color: '#383838'
                            },
                            ticks: {
                                backdropColor: '#fdfaf6',
                                color: '#6b7280',
                                stepSize: 2
                            },
                            suggestedMin: 0,
                            suggestedMax: 10
                        }
                    }
                }
            });
        });
    </script>

</body>
</html>
