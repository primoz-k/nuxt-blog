<template>
  <div class="container">
    <div class="flex flex-col">
      <nuxt-link to="/" class="block text-green-500 border-solid border-b-2 py-2 px-2 border-green-500 mt-8 w-16 self-center">
        Domov
      </nuxt-link>
      <button
        @click="toggle"
        class="absolute top-0 bg-green-500 hover:bg-green-700 text-white py-1 px-2 md:py-2 md:px-4 rounded mt-5 text-xs md:text-md l-toggle-button"
      >{{$colorMode.value == 'light' ? 'Lights off' : 'Lights on'}}</button>
      <h1 class="b-title dark:text-gray-100 mt-5">Kalkulator sestavin za kruh</h1>
      <h2 class="b-subtitle dark:text-gray-300 mt-1">Kruh hočem rezat</h2>
      <div class="content max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        <p>
          Če želiš vedno narediti enak kruh, brez kakšnih presenečenj, je najbolj pomembno, da upoštevaš enako razmerje sestavin, čas in temperaturo. Sobna temperatura
          ni enaka v vseh kuhinjah, tako, da se lahko kompenzira s časom. Če je topleje, bo čas vzhajanja krajši in obratno. Najlažje je kontrolirati razmerje in količino sestavin,
          zato sem pripravil enostaven kalkulator s katerim si lahko pomagaš pri pripravi sestavin. Kalkulator ima prednastavljeno 72% hidracijo. To pomeni, da na 1000g (1kg) moke uporabiš 72% moke v gramih. 
          Torej 1000g moke in 720g vode. % pri kvasu in soli pomeni identično. Računaš procente glede na 1000g moke. 1000g moke pomeni da boš dobil/a 2 hlebčka. Jaz delam manjše hlebčke in ponavadi enega naenkrat, tako, da uporabim 400g moke. Vpiši 400g moke v kalkulator in izvedel/a boš preostalo maso sestavin.
        </p>
      </div>
      <div class="flex justify-center">
        <bread-calculator />
      </div>

      <h2 class="subtitle mt-5 dark:text-gray-300">Recept</h2>

      <h2 class="b-subtitle dark:text-gray-300 mt-1">Sobotni kruh</h2>

      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        Ta recept je namenjen tistim, ki imate čas čez dan. Sam proces ni dolg, si je pa potrebno vsakič vzeti par minut za dober kruh. Domneva tudi, da uporabljaš belo moko. Če uporabljaš polbelo ali dodaš polnoyrnato, si v kalkulatorju povečaj procent hidracije na 75%.
      </p>
      <br>

      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4"><strong>**slike in podrobnosti postopka sledijo kmalu**</strong></p>
      <p class="max-w-3xl text-left mt-3 mb-5 dark:text-gray-100 px-4">
        Začneš npr. ob 9:30 zjutraj:
        <br>
        <br>
        1.) <strong>Avtoliza</strong> Najprej se naredi t.i. avtolizo. Sliši se bolj komplicirano, kot v resnici je. Pomeni samo to, da se v prozorni posodi zmeša vsa moka in voda (prozorna zato, da lažje spremljaš testo od strani).
        Voda naj bo okoli 32°C-35°C, če je sobna temperatura med 21°C in 24°C. Moko in vodo zmešaš kar z rokami, toliko, da se moka popolnoma zmeša z vodo, pokriješ in pustiš počivati približno 30 minut.
        <br>
        <br>
        2.) <strong>Mesenje</strong> Po pol ure povrhu mase enakomerno potreseš sol in kvas in z vlažnimi rokami zmešaš vse sestavine. Če se ti testo začne preveč prijemati rok, lahko ponovno zmočiš roke. Najlaži proces mesenja je,
        da greš z roko pod maso, jo primeš in povlečeš oz. raztegneš in nato prepogneš nazaj nad maso. Vse skupaj bi moralo trajati okoli 5 minut. Temperatura testa po koncu mesenja bi morala biti okoli 25°C-26°C. Nič hudega, če je kako
        stopinjo preveč, čas vzhajanja bo malenkost krajši.
        <br>
        <br>
        3.) <strong>Prepogibanje</strong> Testo potrebuje približno dve prepogibanji (prvo po 10ih minutah, drugo v naslednji uri). Proces je podoben, kot pri mesenju: Z vlažno roko greš pod testo (tako, da zajameš približno četrtino testa), ga primeš in povlečeš, dokler čutiš, da se ti ne pretrga, nato
        pa ga prepogneš na nasprotno stran. To narediš še približno trikrat za cel krog. Nato pokriješ in pustiš še 4-5 ur počivati oz. dokler ne naraste za 3x.
        <br>
        <br>
        4.) <strong>Razdelitev</strong> V tem koraku je potrebno razdeliti testo na kroglice. Pomokaj površino, roke in rob posode s testom, da boš lažje prenesel/prenesla testo na pomokano površino.
        Nagni posodo in nežno prenesi testo na pult. Pazi, da ga ne boš preveč vlekel/a in trgal/a. Ko imaš testo izven posode, po sredini testa pomokaj, kjer boš razdelil/a testo na 2 dela. To seveda narediš v primeru, če imaš preveč testa za en hlebček. V primeru, da delaš en hlebček, ti testa ni treba razdeliti.
        <br>
        <br>
        5.) <strong>Oblikovanje</strong> Pomokaj posodo v kateri boš vzhajal/a kruh do konca. Oblikuj vsako kroglico testa v bolj napeto kroglico - to najlažje storiš na nepomokani površini. Kroglico daš v posodo in jo še pomokaš po vrhu.
        <br>
        <br>
        6.) <strong>Zadnje vzhajanje</strong> Pokriješ posode s kuhinjsko krpo ali celotno posodo daš v neprodušno plastično vrečko in pustiš še 1h15min vzhajati. Če je sobna temperatura večja, kot 21°C, bo ta čas krajši (okoli ene ure).
        <br><br>
        7.) <strong>Gretje pečice</strong> Vsaj 45 minut preden gre kruh v pečico, daš litoželezni lonec s pokrovom greti v pečico na 245°C. Če boš pekel/a na pladnju, ti tega koraka ni treba narediti, še vseeno pa je potrebno pečico segreti na vsaj 230°C.
        <br>
        <br>
        8.) <strong>Peka kruha</strong> Prevrni kruh iz posode na glavo na pomokan pult ali peki papir. Hlebec daj v lonec, ki ga nato pokriješ, ali na pladenj in nato v pečico. Če uporabljaš pladenj, na dno pečice položi še manjši pladenj z vodo, da se bo v pečici ob peki delala para in vlažila kruh. Če uporabljaš lonec, tega ni potrebno narediti, 
        ker že lonec poskrbi, da se bo kruh pekel v pari. Peči 30 minut, nato pa lonec odkrij in peči še 20 minut. Po koncu peke kruh prestavi na rešetko za hlajenje in pusti kako uro, da se kruh ohladi.
      </p>
    </div>
  </div>
</template>

<script>
import Logo from '~/components/Logo.vue'
import BreadCalculator from '~/components/BreadCalculator.vue'

export default {
  components: {
    Logo,
    BreadCalculator,
  },
  methods: {
    toggle() {
      this.$colorMode.value =
        this.$colorMode.value == 'light' ? 'dark' : 'light'
    }
  }
}
</script>

<style>
/* Sample `apply` at-rules with Tailwind CSS
.container {
  @apply min-h-screen flex justify-center items-center text-center mx-auto;
}
*/
.container {
  /* @apply min-h-screen flex justify-center text-center mx-auto; */
}

.b-title {
  font-family: 'Quicksand', 'Source Sans Pro', -apple-system, BlinkMacSystemFont,
    'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
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
