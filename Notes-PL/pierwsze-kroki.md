# Pierwsze Kroki

Kluczowe jest stworzenie ogólnego przeglądu projektu, obejmującego jego cele oraz sposoby ich realizacji. Należy także zaplanować szczegóły techniczne, budżet, role w zespole oraz terminy.

Oto wstępne pomysły naszego zespołu:

1. **Czujniki**

   * Termometry (wewnętrzny i zewnętrzny)
   * Barometr
   * Higrometr
   * Akcelerometry
   * Kamera
   * Fotodiody
   * Czujnik UV (opcjonalnie)
   * Licznik Geigera (opcjonalnie)
   * Magnetometr (opcjonalnie)
   * Możliwe czujniki zintegrowane w IMU

2. **Komunikacja**

   * Moduł GPS do śledzenia pozycji i prędkości
   * LoRa do przesyłania danych telemetrycznych (433 MHz dla większego zasięgu)
   * GSM do przesyłania danych po lądowaniu (np. SIM808 z GPS, opcjonalnie)
   * Własny system komunikacji (np. zamiast LoRa, opcjonalnie do testów)
   * Antena dookólna na ziemi
   * Dodatkowa antena kierunkowa na ziemi dla lepszego zasięgu (opcjonalnie)

3. **Pojemnik na ładunek**

   * Styrodur na zewnątrz
   * Pianka i folia do izolacji wnętrza
   * Folia Mylar dodatkowo do izolacji
   * wentyl do wyrównania ciśnienia
   * Spadochron

4. **Mikrokontroler**

   * Rozważane są ESP32, Raspberry Pi Zero W lub STM32 w zależności od potrzeb komunikacji, kamery i zasilania
   * Musi obsługiwać logowanie danych z czujników i moduły komunikacyjne
   * Redundantna, druga płytka

### Dane atmosferyczne

Czujniki będą rejestrować warunki na różnych wysokościach. Niektóre dane mogą być przesyłane, jeśli dostępny bitrate będzie wystarczający.

### Śledzenie balonu

GPS będzie śledzić pozycję i prędkość balonu. Dodatkowe czujniki, takie jak akcelerometry, barometry czy magnetometry, mogą dostarczać dane uzupełniające.

### Komunikacja

Do komunikacji na duże odległości można wykorzystać LoRa lub inne rozwiązanie. Ze względu na ograniczony bitrate, pakiety danych muszą być małe i dobrze zaplanowane. Główna antena na ziemi może być dookólna, natomiast opcjonalna antena kierunkowa zapewni większy zasięg.
Po lądowaniu ładunku moduł GSM może wysyłać dane położenia i baterii, logi lub nawet zdjęcia, jeśli sygnał będzie wystarczający. Dane telemetryczne, zdjęcia i logi systemowe będą zapisywane na dwóch kartach microSD dla zapewnienia redundancji.

### Płytka z mikrokontrolerem

Należy zoptymalizować zużycie energii, wagę, moc obliczeniową oraz łatwość implementacji. Obecnie rozważane są Raspberry Pi Zero W, ESP32 oraz STM32.

### Ładunek

Czujniki, baterie, płytki mikrokontrolerów i moduły komunikacyjne będą owinięte w piankę i folię, a następnie umieszczone w skrzynce z Styroduru. Styrodur jest lekki, dobrze izoluje, szeroko dostępny i łatwy w obróbce. Dodatkowo, folia Mylar może wspomóc izolację. Na zewnątrz skrzynki planowane jest umieszczenie niektórych czujników, anteny, spadochronu oraz mocowania balonu. Dodatkowo rozważane jest użycie ogrzewaczy chemicnych.

