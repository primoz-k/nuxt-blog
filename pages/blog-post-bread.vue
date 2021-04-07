<template>
  <div class="container">
    <div class="flex flex-col items-center pb-8">
      <nuxt-link
        to="/"
        class="block text-green-500 border-solid border-b-2 py-2 px-2 border-green-500 mt-8 w-16 self-center"
      >
        Domov
      </nuxt-link>
      <button
        @click="toggle"
        class="absolute top-0 bg-green-500 hover:bg-green-700 text-white py-1 px-2 md:py-2 md:px-4 rounded mt-5 text-xs md:text-md l-toggle-button"
      >
        {{ $colorMode.value == "light" ? "Lights off" : "Lights on" }}
      </button>
      <h1 class="b-title dark:text-gray-100 mt-5">
        Kalkulator sestavin za kruh
      </h1>
      <h2 class="b-subtitle dark:text-gray-300 mt-1">Kruh hočem rezat</h2>
      <div
        class="content max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4 pb-5"
      >
        <p>
          Če želiš vedno narediti enak kruh, brez kakšnih presenečenj, je
          najbolj pomembno, da upoštevaš enako razmerje sestavin, čas in
          temperaturo. Čas vzhajanja je odvisen od sobne temperature, ki ni
          enaka v vseh kuhinjah. Če je topleje, bo čas vzhajanja krajši in
          obratno. Najlažje je kontrolirati razmerje in količino sestavin, zato
          sem pripravil enostaven kalkulator s katerim si lahko pomagaš pri
          pripravi sestavin. Kalkulator ima prednastavljeno 72% hidracijo. To
          pomeni, da na 1000g (1kg) moke uporabiš 72% moke v gramih. Torej 1000g
          moke in 720g vode. Enako velja za % kvasa in soli, ki ju tudi računaš
          glede na 1000g moke. 1000g moke pomeni da boš dobil/a 2 hlebčka. Jaz
          delam manjše hlebčke in ponavadi enega naenkrat, tako, da uporabim
          400g moke. Vpiši 400g moke v kalkulator in izvedel/a boš preostalo
          količino sestavin.
        </p>
      </div>
      <div class="flex flex-col md:flex-row justify-center">
        <bread-calculator />
      </div>

      <h2 class="subtitle mt-5 dark:text-gray-300">Recept</h2>

      <h2 class="b-subtitle dark:text-gray-300 mt-1">Sobotni kruh</h2>

      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        Ta recept je namenjen tistim, ki imate čas čez dan. Sam proces ni dolg,
        si je pa potrebno vsakič vzeti par minut za dober kruh. V receptu
        uporabljam belo moko. Če uporabljaš polbelo ali dodaš polnozrnato, si v
        kalkulatorju povečaj procent hidracije na 75%.
      </p>
      <br />

      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        Začneš npr. ob 9:30 zjutraj:
      </p>
      <br />
      <br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        1.) <strong>Avtoliza</strong> Najprej se naredi t.i. avtolizo. Sliši se
        bolj komplicirano, kot v resnici je. Pomeni samo to, da se v prozorni
        posodi zmeša vsa moka in voda (prozorna zato, da lažje spremljaš testo
        iz strani). Voda naj ima okoli 32°C-35°C, če je sobna temperatura 21°C.
        Če je v sobi topleje, uporabi malce hladnejšo vodo. Moko in vodo mešaš
        kar z rokami toliko časa, da se moka popolnoma poveže z vodo. Pokriješ
        in pustiš počivati približno 30 minut.
      </p>
      <br />
      <div class="flex flex-col md:flex-row items-center justify-center">
        <img
          src="~/assets/images/bread/test_0.jpg"
          class="max-w-xs text-center"
        />
      </div>
      <br /><br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        2.) <strong>Po pol ure</strong> Po vrhu testa enakomerno potreseš sol in
        kvas in z vlažnimi rokami zmešaš vse sestavine. Če se ti testo začne
        preveč prijemati rok, lahko ponovno zmočiš roke. Najlažji proces mesenja
        je, da greš z roko pod testo, ga primeš in povlečeš oz. raztegneš in
        nato prepogneš nazaj nad testo. Vse skupaj bi moralo trajati okoli 5
        minut. Temperatura testa po koncu mesenja bi morala biti okoli
        25°C-26°C. Nič hudega, če je kako stopinjo preveč, le čas vzhajanja bo
        malenkost krajši.
      </p>
      <div class="flex flex-col md:flex-row items-center justify-around">
        <img
          src="~/assets/images/bread/test_2.jpg"
          class="max-w-xs text-center"
        />
        <img
          src="~/assets/images/bread/test_3.jpg"
          class="max-w-xs text-center"
        />
        <img
          src="~/assets/images/bread/test_4.jpg"
          class="max-w-xs text-center"
        />
      </div>
      <br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        3.) <strong>Prepogibanje</strong> Testo potrebuje približno dve
        prepogibanji (prvo po 10ih minutah, drugo v naslednji uri). Proces je
        podoben, kot pri mesenju: Z vlažno roko greš pod testo (tako, da zajameš
        približno četrtino testa), ga primeš in povlečeš, ravno toliko, da se ti
        ne pretrga, nato pa ga prepogneš na nasprotno stran. To narediš še
        približno trikrat za cel krog. Nato pokriješ in pustiš počivati 4-5 ur
        oz. dokler ne naraste za 3x.
      </p>
      <br />
      <br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        4.) <strong>Razdelitev</strong> V tem koraku je potrebno razdeliti testo
        na kroglice. Pomokaj površino, roke in rob posode s testom, da boš lažje
        prenesel/prenesla testo iz posode na pomokan pult. Nagni posodo in nežno
        prenesi testo na pult. Pazi, da ga ne boš preveč vlekel/a in trgal/a. Po
        sredini testa pomokaj tisti del, kjer boš z nožem razdelil/a testo na 2
        dela. To seveda narediš v primeru, če imaš preveč testa za en hlebček. V
        primeru, da delaš en hlebček, ti testa ni treba razdeliti.
      </p>
      <br />
      <br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        5.) <strong>Oblikovanje</strong> Pomokaj čisto posodo v kateri boš
        vzhajal/a kruh do konca. Oblikuj vsako kroglico testa v bolj napeto
        kroglico - to najlažje storiš na nepomokani površini. Kroglico daš v
        posodo in jo še pomokaš po vrhu.
      </p>
      <br />
      <br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        6.) <strong>Zadnje vzhajanje</strong> Posodo lahko pokriješ s kuhinjsko
        krpo ali pa jo daš v neprodušno plastično vrečko in pustiš vzhajati
        1h15min. Če je sobna temperatura večja kot 21°C, bo ta čas krajši (okoli
        ene ure).
      </p>
      <br /><br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        7.) <strong>Gretje pečice</strong> Vsaj 45 minut preden peko kruha,
        vstaviš litoželezni lonec s pokrovom v pečico in segreješ na 245°C. Ko
        pečica doseže temperaturo, pustiš lonec še nekaj minut v pečici, da se
        dobro segreje. Če boš pekel/a na pladnju, ti tega koraka ni treba
        narediti, še vseeno pa je potrebno pečico segreti na vsaj 230°C.
      </p>
      <br />
      <br />
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        8.) <strong>Peka kruha</strong> Prevrni testo iz posode na glavo na
        pomokan pult ali peki papir. Testo skupaj s peki papirjem previdno
        prenesi v lonec (in ga pokrij) oz. na pladenj in nato v pečico. Če
        uporabljaš pladenj, na dno pečice položi še manjši pladenj z vodo, da se
        bo v pečici delala para in med peko vlažila kruh. Če uporabljaš lonec,
        tega ni potrebno narediti, saj za paro poskrbi sam. Peci 30 minut, nato
        odstrani pokrov in peci še 20 minut. Po koncu peke kruh prestavi na
        rešetko za hlajenje in pusti eno uro, da se kruh ohladi.
      </p>
      <div class="flex flex-col md:flex-row items-center justify-center">
        <img
          src="~/assets/images/bread/bread_finish.jpg"
          class="max-w-xs text-center"
        />
      </div>
      <h3 class="text-xl b-title dark:text-gray-100 mt-5">Video</h3>
      <div class="video-container mt-5 flex justify-center items-center">
        <iframe width="560" height="315" src="https://www.youtube.com/embed/9Sn9pxwgT0E" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from "~/components/Logo.vue";
import BreadCalculator from "~/components/BreadCalculator.vue";

export default {
  components: {
    Logo,
    BreadCalculator,
  },
  methods: {
    toggle() {
      this.$colorMode.value =
        this.$colorMode.value == "light" ? "dark" : "light";
    },
  },
};
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex flex-col md:flex-row justify-center items-center text-center mx-auto;
}
*/
.container {
  /* @apply min-h-screen flex flex-col md:flex-row justify-center text-center mx-auto; */
}

.b-title {
  font-family: "Quicksand", "Source Sans Pro", -apple-system, BlinkMacSystemFont,
    "Segoe UI", Roboto, "Helvetica Neue", Arial, sans-serif;
  display: block;
  font-weight: 300;
  font-size: 42px;
  color: #35495e;
  letter-spacing: 1px;
}

.b-subtitle {
  font-weight: 300;
  font-size: 28px;
  color: #526488;
  word-spacing: 5px;
  padding-bottom: 15px;
}

.links {
  padding-top: 15px;
}

.l-toggle-button {
  right: 50px;
}
</style>
