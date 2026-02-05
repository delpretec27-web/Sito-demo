<!DOCTYPE html>
<html lang="it">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>ProSoluzioni | Consulenza Aziendale</title>
  </head>
  <body>
    <div id="root"></div>
    <script type="module" src="/src/main.tsx"></script>
  </body>
</html>

import { Navbar } from "@/components/Navbar";
import { Hero } from "@/components/Hero";
import { Services } from "@/components/Services";
import { Benefits } from "@/components/Benefits";
import { ContactForm } from "@/components/ContactForm";
import { Footer } from "@/components/Footer";

export default function Home() {
  return (
    <div className="min-h-screen bg-slate-50">
      <Navbar />
      <main>
        <Hero />
        <Services />
        <Benefits />
        <ContactForm />
      </main>
      <Footer />
    </div>
  );
}
// Estratto della logica di invio
const onSubmit = (data) => {
  mutation.mutate(data, {
    onSuccess: () => {
      toast({
        title: "Messaggio inviato!",
        description: "Ti ricontatteremo al più presto.",
      });
      form.reset();
    },
  });
};

@tailwind base;
@tailwind components;
@tailwind utilities;

:root {
  --primary: 221 83% 53%;      /* Blu ProSoluzioni */
  --secondary: 224 76% 48%;    /* Blu Scuro */
  --accent: 45 93% 47%;        /* Oro per i dettagli */
  --background: 210 40% 98%;
  --foreground: 222 47% 11%;
  --radius: 0.75rem;
}

body {
  @apply bg-background text-foreground antialiased;
  font-family: 'DM Sans', sans-serif;
}

h1, h2, h3 {
  font-family: 'Outfit', sans-serif;
}
