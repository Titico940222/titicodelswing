<script>
    import HeroSection from "$lib/components/HeroSection.svelte";
    import AboutSection from "$lib/components/AboutSection.svelte";
    import ClassesSection from "$lib/components/ClassesSection.svelte";
    import TeachersSection from "$lib/components/TeachersSection.svelte";
    import TestimonialsSection from "$lib/components/TestimonialsSection.svelte";
    import ContactSection from "$lib/components/ContactSection.svelte";
    import FooterSection from "$lib/components/FooterSection.svelte";
    import WhatsappButton from "$lib/components/WhatsappButton.svelte";

    // Datos de los grupos de baile
    const clases = [
        {
            id: 1,
            titulo: "Grupo Juvenil Básico",
            descripcion:
                "Para jóvenes de 11 a 17 años que quieren iniciarse en los ritmos latinos.",
            icono: "fa-solid fa-child",
            imagen: "/2.jpeg",
            horario: "Martes y Jueves: 4:00-5:00 PM<br/>Sábado: 4:00-5:00 PM",
            edades: "11-17 años",
            mensualidad: "$100.000",
            inscripcion: "$20.000",
        },
        {
            id: 2,
            titulo: "Grupo Juvenil Avanzado",
            descripcion:
                "Para jóvenes de 11 a 17 años con experiencia en baile latino.",
            icono: "fa-solid fa-star",
            imagen: "/3.jpeg",
            horario: "Jueves: 5:00-6:00 PM<br/>Sábado: 4:00-5:00 PM",
            edades: "11-17 años",
            mensualidad: "$80.000",
            inscripcion: "$20.000",
        },
        {
            id: 3,
            titulo: "Grupo Social Tarde",
            descripcion:
                "Para mayores de 14 años que buscan divertirse bailando ritmos latinos.",
            icono: "fa-solid fa-users",
            imagen: "/4.jpeg",
            horario: "Martes, Miércoles y Jueves: 6:10-7:10 PM",
            edades: "14+ años",
            mensualidad: "$100.000",
            inscripcion: "$20.000",
        },
        {
            id: 4,
            titulo: "Grupo Social Noche",
            descripcion:
                "Para mayores de 14 años que prefieren bailar en horario nocturno.",
            icono: "fa-solid fa-moon",
            imagen: "/5.jpeg",
            horario: "Martes, Miércoles y Jueves: 7:10-8:10 PM",
            edades: "14+ años",
            mensualidad: "$100.000",
            inscripcion: "$20.000",
        },
        {
            id: 5,
            titulo: "Grupo Base Profesional",
            descripcion:
                "Para mayores de 14 años con nivel avanzado. Requiere audición previa.",
            icono: "fa-solid fa-trophy",
            imagen: "/6.jpeg",
            horario: "Lunes, Miércoles y Viernes: 7:00-8:30 PM",
            edades: "14+ años",
            mensualidad: "$100.000",
            inscripcion: "$20.000",
            nota: "Previa audición",
        },
    ];

    // Datos de los profesores
    const profesores = [
        {
            id: 1,
            nombre: "Javier Iván Narváez",
            especialidad: "Mercadólogo y Coreógrafo",
            experiencia: "Bailarín Profesional",
            foto: "/JAVIER NARVAEZ.jpeg",
        },
        {
            id: 2,
            nombre: "Luis Hidalgo",
            especialidad: "Licenciado en Educación Física y Coreógrafo",
            experiencia: "Bailarín Profesional",
            foto: "/LUIS HIDALGO.jpeg",
        },
    ];
</script>

<svelte:head>
    <link rel="stylesheet" href="https://unpkg.com/aos@next/dist/aos.css" />
    <title>Titicó del Swing - Academia de Baile Latino</title>
    <meta
        name="description"
        content="Academia de baile especializada en ritmos latinos como salsa, merengue y bachata. Clases para todos los niveles en un ambiente divertido y profesional en Pasto, Nariño."
    />
</svelte:head>

<HeroSection />
<AboutSection />
<ClassesSection {clases} />
<TeachersSection {profesores} />
<ContactSection />
<FooterSection />
<WhatsappButton />
