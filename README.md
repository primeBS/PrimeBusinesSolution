import React from "react";
import { Card, CardContent } from "@/components/ui/card";
import { Button } from "@/components/ui/button";

const services = [
  {
    title: "Urejanje socialnih omrežij",
    examples: [
      "Instagram profil za modno znamko",
      "Facebook stran lokalne trgovine",
      "TikTok kampanja za startup",
      "LinkedIn profil za podjetnika",
      "Pinterest tabla za notranje oblikovanje"
    ]
  },
  {
    title: "Urejanje slik in videjev",
    examples: [
      "Promo video za dogodek",
      "Fotografije izdelkov (pred/po)",
      "Intro/outro za YouTube",
      "Highlight video za športno ekipo",
      "Umetniško retuširanje portretov"
    ]
  },
  {
    title: "Marketing",
    examples: [
      "Email kampanja za e-trgovino",
      "SEO optimizacija spletne strani",
      "Google Ads za lokalne storitve",
      "Družbena analiza konkurence",
      "Strategija vsebinskega marketinga"
    ]
  },
  {
    title: "Transkripcija",
    examples: [
      "Sestanek Zoom (30min)",
      "Podcast epizoda (audio -> tekst)",
      "Intervjuji za raziskavo",
      "Prepis spletnega seminarja",
      "Dvojezicni prepis (slovensko/angleško)"
    ]
  },
  {
    title: "Pisanje",
    examples: [
      "Blog objava (SEO optimizirana)",
      "Opis izdelka za spletno trgovino",
      "Tekst za oglas",
      "Uvodna predstavitev podjetja",
      "Scenarij za video oglas"
    ]
  },
  {
    title: "Preizkušanje iger",
    examples: [
      "Test mobilne igre (Android)",
      "Beta test RPG igre",
      "Poročilo o hroščih",
      "Test uporabniške izkušnje",
      "Ocena igranja in idej za izboljšave"
    ]
  }
];

const testimonials = [
  {
    name: "Ana M.",
    feedback: "Ekipa Prime BusinessSolution mi je popolnoma prenovila Instagram – izgled in strategija sta zdaj vrhunska!"
  },
  {
    name: "Tomaž K.",
    feedback: "Sodelovanje pri montaži videov je bilo profesionalno in hitro. Z rezultatom sem zelo zadovoljen."
  },
  {
    name: "Eva L.",
    feedback: "Zahvaljujoč njihovi marketinški strategiji se je obisk moje spletne trgovine podvojil."
  },
  {
    name: "Marko P.",
    feedback: "Preizkusili so mojo igro in mi dali izjemno uporabne povratne informacije. Toplo priporočam!"
  },
  {
    name: "Sara Z.",
    feedback: "Prejeli smo natančne prepise vseh naših intervjujev. Storitev je bila hitra in zanesljiva."
  }
];

export default function PrimeBusinessSolution() {
  return (
    <main className="min-h-screen bg-gradient-to-br from-gray-900 via-gray-800 to-gray-900 text-white px-6 py-12">
      <div className="max-w-6xl mx-auto">
        <h1 className="text-4xl font-bold mb-6 text-center">Prime BusinessSolution</h1>
        <p className="text-center mb-12 text-gray-300 text-lg max-w-3xl mx-auto">
          Ponuja vrhunske digitalne storitve: od urejanja socialnih omrežij in vizualnih vsebin do marketinga, pisanja in testiranja iger. Najemite nas za profesionalne in sodobne rešitve.
        </p>
        <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-8 mb-16">
          {services.map((service, index) => (
            <Card key={index} className="bg-gray-800 border-gray-700">
              <CardContent className="p-6">
                <h2 className="text-2xl font-semibold mb-4 text-primary">
                  {service.title}
                </h2>
                <ul className="list-disc list-inside space-y-2 text-gray-300">
                  {service.examples.map((example, i) => (
                    <li key={i}>{example}</li>
                  ))}
                </ul>
                <Button className="mt-6 w-full bg-primary text-white hover:bg-primary/80">
                  Najemi nas
                </Button>
              </CardContent>
            </Card>
          ))}
        </div>

        <section className="bg-gray-800 rounded-2xl p-8 shadow-lg mb-16">
          <h2 className="text-3xl font-bold text-center mb-6">Mnenja zadovoljnih strank</h2>
          <div className="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3 gap-6">
            {testimonials.map((testimonial, index) => (
              <div key={index} className="bg-gray-900 p-6 rounded-xl shadow-md">
                <p className="text-gray-300 mb-4 italic">"{testimonial.feedback}"</p>
                <p className="text-primary font-semibold text-right">- {testimonial.name}</p>
              </div>
            ))}
          </div>
        </section>

        <section className="bg-gray-800 rounded-2xl p-8 shadow-lg">
          <h2 className="text-3xl font-bold text-center mb-6">Kontaktirajte nas</h2>
          <p className="text-center text-gray-400 mb-4">
            Lahko nas kontaktirate tudi neposredno preko e-pošte: <a href="mailto:primeb689@gmail.com" className="text-primary underline">primeb689@gmail.com</a>
          </p>
          <form action="https://formspree.io/f/xkgrrjdj" method="POST" className="max-w-2xl mx-auto space-y-6">
            <div>
              <label className="block mb-2 text-gray-300" htmlFor="name">Ime</label>
              <input name="name" id="name" type="text" required className="w-full p-3 rounded-md bg-gray-900 text-white border border-gray-700" placeholder="Vaše ime" />
            </div>
            <div>
              <label className="block mb-2 text-gray-300" htmlFor="email">Email</label>
              <input name="email" id="email" type="email" required className="w-full p-3 rounded-md bg-gray-900 text-white border border-gray-700" placeholder="vaš@email.si" />
            </div>
            <div>
              <label className="block mb-2 text-gray-300" htmlFor="message">Sporočilo</label>
              <textarea name="message" id="message" rows="5" required className="w-full p-3 rounded-md bg-gray-900 text-white border border-gray-700" placeholder="Vaše sporočilo..."></textarea>
            </div>
            <Button type="submit" className="w-full bg-primary text-white hover:bg-primary/80">
              Pošlji sporočilo
            </Button>
          </form>
        </section>
      </div>
    </main>
  );
}
