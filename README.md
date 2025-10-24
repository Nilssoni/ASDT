# ASDT
Advanced Software Development Techniques 2025

#### 1) Rinnakkainen prosessitoteutus
Käytetään fork()-kutsua luomaan useita lapsiprosesseja.
Jokainen lapsiprosessi kutsuu aloitaRotta()-funktiota itsenäisesti.
Parent-prosessi odottaa wait(NULL)-kutsuilla kaikkien rottien valmistumista.
Jaettu muisti (shmget, shmat).

#### 2) Rinnakkainen säietoteutus
Käytetään C++ std::thread-rakennetta.
Jokainen säie kutsuu aloitaRotta()-funktiota.
main() säie odottaa kaikkien säikeiden valmistumista join()-kutsuilla.
Tulostus on suojattu mutex-lukolla (lock_guard).

#### 3) Prosessien välinen jaetun muistin toteutus + eksklusiivinen kirjoitus
Labyrintti on siirretty jaettuun muistiin (jaettuLabyrintti).

#### 4) Säikeiden välinen eksklusiivisuus
Tulostus on suojattu mutex-rakenteella.

#### 5) Prosessien suspend-toiminnallisuus
Toimiva prosessien systeemin suspend-toiminnalisuus jäädytetyn labyrinttitilanteen talteenottamista varten
