---
title: Jak skonfigurować Cloudflare CDN (Poradnik 2027)
slug: clou
date: 2026-11-24
draft: false
---
Jak skonfigurować Cloudflare CDN (Poradnik 2027)

Cloudflare CDN to popularne rozwiązanie, które pozwala poprawić wydajność stron internetowych, skrócić czas ładowania i zapewnić dodatkową warstwę ochrony. Dzięki globalnej sieci serwerów Cloudflare właściciele stron mogą przechowywać statyczne treści w pamięci podręcznej, chronić swoje serwery i optymalizować dostęp do witryn dla użytkowników z różnych regionów świata.

Niezależnie od tego, czy prowadzisz blog WordPress, stronę firmową, sklep internetowy czy witrynę na serwerze VPS, konfiguracja Cloudflare CDN może pomóc zwiększyć wydajność Twojej strony.

W tym poradniku dowiesz się, jak skonfigurować Cloudflare CDN w 2027 roku, podłączyć domenę, ustawić rekordy DNS, aktywować proxy, skonfigurować pamięć podręczną oraz rozwiązywać najczęstsze problemy.

Jeśli korzystasz również z narzędzi do płatności internetowych za usługi międzynarodowe, możesz zapoznać się z CoinePay jako jedną z dostępnych opcji płatności online.

👉 **CoinePay 官方入口：**  
[https://www.coinepay.net/register?referrer=RFGSSDZ9](https://www.coinepay.net/register?referrer=RFGSSDZ9)

Jeśli korzystasz również z sieci TRON do przesyłania USDT, możesz poznać usługę wynajmu energii TRON oferowaną przez TRXAPI. W przypadku obsługiwanych transakcji może ona pomóc ograniczyć zużycie zasobów TRX.

👉 **TRXAPI 官方入口：**  
[https://login.trxapi.io/energy](https://login.trxapi.io/energy)

## **Czym jest Cloudflare CDN?**

Cloudflare CDN to sieć dostarczania treści, która umożliwia dystrybucję zasobów strony internetowej za pośrednictwem globalnej sieci serwerów. Zamiast łączyć każdego użytkownika bezpośrednio z serwerem źródłowym, Cloudflare może dostarczać zapisane w pamięci podręcznej treści z lokalizacji znajdującej się bliżej odwiedzającego.

Cloudflare oferuje również dodatkowe usługi, takie jak zarządzanie DNS, ochrona przed atakami DDoS, filtrowanie ruchu, obsługa SSL/TLS oraz różne funkcje buforowania danych.

Najważniejsze zalety Cloudflare CDN:

- Szybsze ładowanie stron dla użytkowników z różnych regionów.
- Mniejsze zużycie przepustowości serwera źródłowego.
- Dodatkowa ochrona przed określonym rodzajem złośliwego ruchu i atakami DDoS.
- Obsługa szyfrowania SSL/TLS.
- Elastyczne zarządzanie DNS.
- Funkcje buforowania i optymalizacji stron internetowych.

Cloudflare oferuje zarówno bezpłatne, jak i płatne plany. Wiele podstawowych funkcji CDN można skonfigurować w ramach bezpłatnego planu Free.

## **Co przygotować przed konfiguracją Cloudflare CDN?**

Zanim podłączysz swoją stronę do Cloudflare, upewnij się, że masz:

- Zarejestrowaną nazwę domeny.
- Działającą stronę internetową lub serwer hostingowy.
- Dostęp do panelu zarządzania u rejestratora domeny.
- Dostęp do rekordów DNS swojej domeny.
- Adres IP serwera hostingowego, jeśli jest wymagany.

Jeśli domena jest już połączona ze stroną internetową, przed wprowadzeniem zmian sprawdź istniejącą konfigurację DNS. Nieprawidłowe rekordy DNS mogą spowodować niedostępność strony, poczty elektronicznej lub innych usług.

## **Krok 1: Utwórz konto Cloudflare**

Najpierw przejdź na oficjalną stronę Cloudflare:

[https://www.cloudflare.com/](https://www.cloudflare.com/)

Utwórz konto, podając swój adres e-mail i hasło.

Po rejestracji zaloguj się do panelu Cloudflare. Będziesz mógł dodać domenę oraz skonfigurować ustawienia DNS, zabezpieczenia, pamięci podręcznej i inne funkcje.

## **Krok 2: Dodaj domenę do Cloudflare**

Po zalogowaniu:

1. Otwórz panel Cloudflare.
2. Wybierz opcję dodawania lub podłączania domeny.
3. Wpisz nazwę swojej domeny, na przykład [example.com](http://example.com).
4. Przejdź do następnego kroku.
5. Wybierz odpowiedni plan.

W przypadku większości prywatnych stron, blogów i niewielkich witryn dobrym rozwiązaniem na początek jest plan Free.

Cloudflare spróbuje automatycznie wykryć istniejące rekordy DNS i zaimportować je do swojego panelu zarządzania DNS.

## **Krok 3: Sprawdź rekordy DNS**

Przed aktywacją Cloudflare dokładnie sprawdź rekordy DNS.

Najczęściej używane typy rekordów DNS to:

- Rekord A: wskazuje domenę lub subdomenę na adres IPv4.
- Rekord AAAA: wskazuje domenę lub subdomenę na adres IPv6.
- Rekord CNAME: wskazuje domenę lub subdomenę na inną nazwę hosta.
- Rekord MX: określa serwery pocztowe dla domeny.
- Rekord TXT: służy do weryfikacji domeny oraz konfiguracji SPF, DKIM, DMARC i innych usług.

Upewnij się, że główne rekordy Twojej strony są prawidłowe.

Przykład:

Rekord A

Nazwa: @

Wartość: adres IP Twojego serwera

Rekord CNAME

Nazwa: www

Wartość: główna domena lub nazwa hosta podana przez dostawcę hostingu.

Dokładna konfiguracja zależy od ustawień Twojego hostingu.

Jeśli korzystasz z poczty elektronicznej powiązanej z domeną, upewnij się, że rekordy MX, TXT i pozostałe rekordy związane z pocztą są prawidłowo skonfigurowane. Proxy Cloudflare nie obsługuje standardowego ruchu pocztowego, dlatego rekordy pocztowe powinny zazwyczaj pozostać w trybie DNS Only.

## **Krok 4: Włącz proxy Cloudflare**

Jednym z najważniejszych etapów konfiguracji Cloudflare CDN jest aktywowanie usługi proxy.

W sekcji zarządzania DNS znajdziesz opcję określającą status proxy dla obsługiwanych rekordów.

Proxied — pomarańczowa chmura

Po włączeniu pomarańczowej chmury ruch dla obsługiwanych rekordów przechodzi przez Cloudflare. Dzięki temu można korzystać z odpowiednich funkcji CDN, zabezpieczeń i proxy.

DNS Only — szara chmura

Po wybraniu szarej chmury Cloudflare zapewnia jedynie rozwiązywanie nazw DNS. Ruch nie jest przekazywany przez sieć proxy Cloudflare.

W przypadku głównych rekordów strony, takich jak rekord A domeny oraz rekord A lub CNAME dla www, włącz opcję Proxied, jeśli Twoja konfiguracja strony na to pozwala.

Nie włączaj proxy automatycznie dla wszystkich rekordów DNS. Niektóre usługi, w tym poczta elektroniczna, rekordy weryfikacyjne i wybrane usługi zewnętrzne, powinny pozostać w trybie DNS Only.

## **Krok 5: Zmień serwery nazw domeny**

Po sprawdzeniu rekordów DNS Cloudflare udostępni Ci dwa serwery nazw (nameservers).

Musisz zastąpić obecne serwery nazw domeny tymi, które zostały przypisane przez Cloudflare.

Proces wygląda zazwyczaj następująco:

1. Zaloguj się na konto u rejestratora domeny.
2. Otwórz stronę zarządzania domeną.
3. Znajdź ustawienia serwerów nazw.
4. Zastąp obecne serwery nazw dwoma serwerami podanymi przez Cloudflare.
5. Zapisz zmiany.

Propagacja zmian serwerów nazw może potrwać pewien czas.

W tym okresie rozwiązywanie nazw DNS może się różnić w zależności od sieci i pamięci podręcznej DNS. Unikaj niepotrzebnych zmian DNS podczas aktywacji.

Jeśli DNSSEC jest włączony dla Twojej domeny, sprawdź jego konfigurację przed zmianą serwerów nazw. Nieprawidłowe ustawienia DNSSEC mogą uniemożliwić prawidłowe rozwiązywanie domeny.

## **Krok 6: Skonfiguruj SSL/TLS**

SSL/TLS jest ważny dla zabezpieczenia połączeń ze stroną internetową i uniknięcia ostrzeżeń bezpieczeństwa w przeglądarkach.

W panelu Cloudflare:

1. Wybierz swoją domenę.
2. Otwórz sekcję SSL/TLS.
3. Sprawdź tryb szyfrowania.
4. Wybierz tryb odpowiadający konfiguracji SSL na serwerze źródłowym.

Cloudflare oferuje zazwyczaj następujące tryby SSL/TLS:

Flexible

Tryb Flexible szyfruje połączenie między użytkownikami a Cloudflare, ale połączenie między Cloudflare a serwerem źródłowym nie jest szyfrowane.

Można go używać, gdy serwer źródłowy nie posiada certyfikatu SSL, jednak zazwyczaj nie jest to zalecane rozwiązanie długoterminowe.

Full

Tryb Full szyfruje połączenie między Cloudflare a serwerem źródłowym. Serwer musi obsługiwać HTTPS, ale certyfikat nie musi być wystawiony przez publicznie zaufany urząd certyfikacji.

Full (Strict)

Tryb Full (Strict) szyfruje połączenie i weryfikuje certyfikat serwera źródłowego. Serwer musi posiadać ważny certyfikat spełniający wymagania Cloudflare.

W przypadku większości stron z prawidłowo skonfigurowanym HTTPS zalecany jest tryb Full (Strict).

Przed jego włączeniem upewnij się, że serwer źródłowy posiada ważny certyfikat SSL.

## **Krok 7: Skonfiguruj pamięć podręczną Cloudflare**

Pamięć podręczna Cloudflare umożliwia przechowywanie wybranych zasobów strony w sieci Cloudflare. Dzięki temu mogą być one dostarczane użytkownikom bez konieczności każdorazowego pobierania ich z serwera źródłowego.

Aby skonfigurować pamięć podręczną:

1. Otwórz swoją domenę w panelu Cloudflare.
2. Przejdź do ustawień pamięci podręcznej.
3. Sprawdź dostępne opcje.
4. Dostosuj działanie pamięci podręcznej do potrzeb swojej strony.

Do zasobów statycznych, które zwykle można buforować, należą:

- Obrazy.
- Pliki CSS.
- Pliki JavaScript.
- Czcionki.
- Statyczne strony HTML, jeśli jest to odpowiednie.

Treści dynamiczne, strony logowania, koszyki zakupowe, panele użytkowników i treści personalizowane wymagają bardziej ostrożnej konfiguracji.

W przypadku stron WordPress unikaj bezwarunkowego buforowania stron zawierających dane logowania, informacje przypisane do użytkowników, zawartość koszyka zakupowego lub funkcje administracyjne.

Możesz wykorzystać Cache Rules w Cloudflare, aby określić, które adresy URL mają być buforowane i w jaki sposób ma działać pamięć podręczna.

## **Krok 8: Skonfiguruj Cache Rules**

Cache Rules umożliwiają kontrolowanie działania pamięci podręcznej dla określonych adresów URL lub warunków.

Możesz na przykład:

- Przechowywać pliki statyczne w pamięci podręcznej przez dłuższy czas.
- Wykluczyć strony administracyjne z buforowania.
- Wyłączyć buforowanie stron logowania.
- Zastosować różne ustawienia pamięci podręcznej dla wybranych subdomen.
- Kontrolować buforowanie określonych typów treści.

Jeśli korzystasz z WordPress, rozważ wykluczenie następujących ścieżek z pamięci podręcznej, jeśli jest to konieczne:

- /wp-admin/
- /wp-login.php

W zależności od konfiguracji strony może być również konieczne wykluczenie stron dynamicznych, stron płatności lub treści personalizowanych.

Po każdej zmianie Cache Rules przetestuj działanie swojej strony.

## **Krok 9: Wyczyść pamięć podręczną Cloudflare**

Jeśli aktualizujesz swoją stronę, ale odwiedzający nadal widzą starą wersję treści, przyczyną może być pamięć podręczna.

Możesz wyczyścić ją bezpośrednio w Cloudflare.

1. Otwórz panel Cloudflare.
2. Wybierz swoją domenę.
3. Przejdź do sekcji pamięci podręcznej.
4. Znajdź opcję czyszczenia pamięci podręcznej.
5. Wybierz odpowiednią metodę czyszczenia.

Cloudflare oferuje różne sposoby usuwania zapisanych treści. W zależności od potrzeb możesz wyczyścić pamięć podręczną dla wybranych adresów URL lub usunąć większy zakres danych.

W przypadku zwykłych aktualizacji strony zazwyczaj lepiej wyczyścić tylko pamięć podręczną zmienionych adresów URL, zamiast usuwać całą zawartość cache.

## **Krok 10: Przetestuj Cloudflare CDN**

Po zakończeniu konfiguracji Cloudflare sprawdź, czy Twoja strona działa prawidłowo.

Zwróć uwagę na następujące kwestie:

- Strona otwiera się bez problemów.
- HTTPS działa bez ostrzeżeń przeglądarki.
- Rekordy DNS są prawidłowo rozwiązywane.
- Wersje domeny z www i bez www działają zgodnie z oczekiwaniami.
- Usługi poczty elektronicznej nadal działają.
- Zasoby statyczne są buforowane tam, gdzie jest to wymagane.

Możesz również sprawdzić nagłówki odpowiedzi HTTP.

Na przykład może pojawić się następujący nagłówek:

cf-cache-status

Najczęściej spotykane wartości to:

- HIT: żądany zasób został dostarczony z pamięci podręcznej.
- MISS: zasobu nie było w pamięci podręcznej, więc został pobrany z serwera źródłowego.
- BYPASS: pamięć podręczna została pominięta.
- DYNAMIC: zasób nie kwalifikuje się do standardowego buforowania.
- EXPIRED: zapisany zasób wygasł.

Nie każde żądanie musi zwracać status HIT. Strony dynamiczne i zasoby nieobjęte buforowaniem mogą prawidłowo zwracać inne wartości.

Możesz również skorzystać z narzędzi do testowania wydajności, takich jak PageSpeed Insights, GTmetrix lub WebPageTest, aby ocenić szybkość ładowania i wydajność swojej strony.

## **Najczęstsze problemy z Cloudflare CDN**

### **Błąd Cloudflare 521**

Błąd 521 zazwyczaj oznacza, że Cloudflare nie może nawiązać połączenia z serwerem źródłowym, ponieważ serwer odrzuca połączenie.

Możliwe rozwiązania:

- Sprawdź, czy serwer działa prawidłowo.
- Upewnij się, że zapora sieciowa zezwala na ruch z Cloudflare.
- Sprawdź usługę WWW na serwerze źródłowym.
- Przejrzyj reguły zapory i oprogramowania zabezpieczającego.

### **Błąd Cloudflare 522**

Błąd 522 oznacza przekroczenie czasu oczekiwania na połączenie między Cloudflare a serwerem źródłowym.

Możliwe przyczyny:

- Przeciążenie serwera źródłowego.
- Reguły zapory blokujące Cloudflare.
- Problemy z łącznością sieciową.
- Zbyt długi czas odpowiedzi serwera.

Sprawdź swój serwer hostingowy i konfigurację sieci.

### **Błędy certyfikatu SSL**

Błędy SSL mogą wystąpić, gdy konfiguracja SSL/TLS w Cloudflare nie odpowiada konfiguracji certyfikatu na serwerze źródłowym.

Sprawdź następujące elementy:

- Certyfikat SSL serwera źródłowego jest ważny.
- Wybrany tryb SSL/TLS jest odpowiedni.
- HTTPS jest prawidłowo skonfigurowany na serwerze źródłowym.
- Nie występują niezgodne reguły przekierowań.

### **Treści na stronie nie aktualizują się**

Jeśli Twoja strona nadal wyświetla stare treści:

- Wyczyść odpowiednią pamięć podręczną Cloudflare.
- Wyczyść pamięć podręczną przeglądarki.
- Sprawdź Cache Rules.
- Upewnij się, czy przyczyną problemu nie jest wtyczka cache na Twojej stronie.

## **Czy Cloudflare CDN jest darmowy?**

Cloudflare oferuje plan Free, który obejmuje różne funkcje DNS, proxy, bezpieczeństwa i buforowania.

Dla wielu prywatnych stron, blogów i małych witryn firmowych plan Free jest wystarczający na początek.

Płatne plany zapewniają dodatkowe funkcje i usługi, w zależności od wybranego pakietu i aktualnej dostępności produktów.

Wybór odpowiedniego planu zależy od ruchu na stronie, wymagań dotyczących bezpieczeństwa, potrzeb związanych z wydajnością oraz budżetu.

## **Lista kontrolna konfiguracji Cloudflare CDN**

Przed zakończeniem konfiguracji sprawdź następujące punkty:

- Domena została dodana do Cloudflare.
- Rekordy DNS zostały sprawdzone.
- Główne rekordy strony są prawidłowo skonfigurowane.
- Proxy jest włączone dla obsługiwanych rekordów strony.
- Serwery nazw zostały zaktualizowane.
- SSL/TLS jest prawidłowo skonfigurowany.
- Ustawienia pamięci podręcznej zostały sprawdzone.
- Strony dynamiczne nie są nieprawidłowo buforowane.
- Strona poprawnie ładuje się przez HTTPS.
- Rekordy DNS poczty elektronicznej nadal są prawidłowe.
- Wydajność strony została przetestowana.

## **Podsumowanie**

Konfiguracja Cloudflare CDN to praktyczny sposób na poprawę dostarczania treści strony internetowej, zarządzanie DNS i dodanie dodatkowej warstwy ochrony.

Podstawowy proces obejmuje dodanie domeny do Cloudflare, sprawdzenie rekordów DNS, aktywowanie proxy, aktualizację serwerów nazw, konfigurację SSL/TLS oraz dostosowanie reguł pamięci podręcznej.

Chociaż Cloudflare oferuje wiele zaawansowanych funkcji, początkujący użytkownicy mogą rozpocząć od podstawowej konfiguracji i stopniowo optymalizować swoją stronę zgodnie z potrzebami.

Prawidłowa konfiguracja DNS, proxy, SSL/TLS i pamięci podręcznej pozwala stworzyć wydajniejszą infrastrukturę internetową i poprawić komfort korzystania ze strony przez użytkowników z różnych regionów świata.

Oficjalne materiały Cloudflare:

Dodawanie domeny do Cloudflare:  
[https://developers.cloudflare.com/fundamentals/manage-domains/add-site/](https://developers.cloudflare.com/fundamentals/manage-domains/add-site/)

Status proxy Cloudflare:  
[https://developers.cloudflare.com/dns/proxy-status/](https://developers.cloudflare.com/dns/proxy-status/)

Cache Rules Cloudflare:  
[https://developers.cloudflare.com/cache/how-to/cache-rules/](https://developers.cloudflare.com/cache/how-to/cache-rules/)

Czyszczenie pamięci podręcznej Cloudflare:  
[https://developers.cloudflare.com/cache/how-to/purge-cache/](https://developers.cloudflare.com/cache/how-to/purge-cache/)