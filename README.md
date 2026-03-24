# Dokumentacja projektu z przedmiotu Środowiska Udostępniania Usług

## Temat projektu: MCP Grafana (akronim MCP-G)

## Autorzy:
- Mateusz Górski
- Mateusz Lampert
- Wojciech Michaluk
- Jan Pawlica

## Rok 2025/26, grupa 5 - piątek 13:15

## Spis treści
1. [Wprowadzenie](#rozdział-1-wprowadzenie)
   1. [Kubernetes](#kubernetes)
   2. [Grafana](#grafana)
   3. [MCP](#mcp)
2. [Podstawy teoretyczne i stos technologiczny](#rozdział-2-podstawy-teoretyczne-i-stos-technologiczny)
3. [Opis studium przypadku](#rozdział-3-opis-studium-przypadku)
4. [Architektura rozwiązania](#rozdział-4-architektura-rozwiązania)
5. [Konfiguracja środowiska](#rozdział-5-konfiguracja-środowiska)
6. [Sposób instalacji](#rozdział-6-sposób-instalacji)
7. [Etapy wdrażania demo](#rozdział-7-etapy-wdrażania-demo)
   1. [Konfiguracja](#konfiguracja)
   2. [Przygotowanie danych](#przygotowanie-danych)
8. [Opis demo](#rozdział-8-opis-demo)
   1. [Procedura wykonania](#procedura-wykonania)
   2. [Wyniki](#wyniki)
9. [Podsumowanie i wnioski](#rozdział-9-podsumowanie-i-wnioski)
10. [Referencje](#rozdział-10-referencje)

## Rozdział 1: Wprowadzenie

Celem tego projektu jest demonstracja wykorzystania serwera MCP dla Grafany do sterowania aplikacją
Grafany z poziomu wybranego modelu LLM.
Aplikacja demonstracyjna powinna zostać wdrożona w klastrze Kubernetesa w celu generowania danych
wizualizowanych przez Grafanę.

### Kubernetes

Kubernetes (**K8s**) to otwartoźródłowa platforma, która ułatwia automatyzację wdrażania, skalowania
i zarządzania skonteneryzowanymi aplikacjami.
Jest to najpopularniejsze narzędzie w środowiskach DevOps do zarządzania złożonymi aplikacjami
rozproszonymi.
System ten pozwala na uruchamianie i zarządzanie setkami, a nawet tysiącami kontenerów.
Kubernetes cechuje się również samonaprawianiem (self-healing), czyli automatycznym restartem
wadliwych kontenerów, które uległy awarii, ewentualnie nawet ich wymianą w razie potrzeby.
Jego działanie opiera się na organizacji kontenerów w tzw. *pody*, czyli logiczne grupy, co ułatwia
zarządzanie aplikacją.

Warto wspomnieć, czym Kubernetes **nie jest**, aby dostrzec pełnię jego zalet.
Nie jest to tradycyjny, "zawierający wszystko" system *Platform as a Service* (PaaS), ale posiada
funkcjonalności ogólnego zastosowania, które cechują rozwiązania tego typu.
Obejmują one instalacje (*deployments*), a także skalowanie i balansowanie ruchu, co umożliwia
użytkownikom integrację rozwiązań służących do logowania, monitoringu i ostrzegania.
Kubernetes również **nie jest monolitem** - dostarcza elementy, z których można zbudować aplikację,
ale są one opcjonalne i funkcjonują na zasadzie wtyczek.
Pozostawia to użytkownikowi wybór i elastyczność, bowiem Kubernetes:
- nie ogranicza obsługiwanych typów aplikacji,
- nie wymusza użycia konkretnych systemów zbierania logów, monitorowania ani ostrzegania,
- eliminuje konieczność orchestracji i scentralizowanego zarządzania.

### Grafana

Grafana to popularna, również otwartoźródłowa platforma, która służy do wizualizacji danych,
monitorowania infrastruktury IT oraz analizy w czasie rzeczywistym.
Umożliwia tworzenie interaktywnych dashboardów z np. wykresami, panelami i alertami, a także
integrację danych z różnych źródeł, m.in. Prometheus, InfluxDB, MySQL czy ElasticSearch.
Rysunek poniżej ([źródło](https://grafana-docs.readthedocs.io/en/latest/ds_adddatasource.html)) przedstawia panel wyboru źródła danych w Grafanie, obejmujący wiele popularnych
baz danych i rozwiązań chmurowych.
![Widok wyboru źródła danych](./images/grafana_data_sources.png)

Kluczowe cechy i zastosowania Grafany obejmują:
- wizualizację złożonych danych z wykorzystaniem szerokiej gamy wykresów (np. słupkowe, liniowe,
*heatmapy*),
- wsparcie dla wielu źródeł danych (patrz rysunek powyżej),
- monitorowanie w czasie rzeczywistym - np. śledzenie wydajności serwerów, aplikacji i usług,
- alerty - powiadomienia dotyczące m.in. anomalii czy przekroczeniu ustalonych progów,
- elastyczność - możliwość działania na serwerach lokalnych oraz w chmurze, rozbudowa przez wtyczki.

### MCP

MCP, czyli _Model Context Protocol_, to otwarty standard technologiczny, który umożliwia modelom LLM
łączyć się w bezpieczny sposób z zewnętrznymi danymi, bazami danych oraz narzędziami programistycznymi.
Dzięki temu zyskał dużą popularność, bo rozwiązał kluczowy problem braku standaryzacji w łączeniu
modeli z zewnętrznymi danymi i narzędziami.
Ułatwia zarządzanie uprawnieniami dzięki ustrukturyzowanemu dostępowi do danych.
MCP działa w modelu klient-serwer.
Serwer udostępnia zasoby (dane), narzędzia oraz prompty, które pełnią rolę reużywalnych szablonów,
instrukcji, z kolei klienci odkrywają i wykorzystują te elementy udostępniane przez serwery.
Każdy klient utrzymuje połączenie 1:1 z poszczególnym serwerem.
Całość jest zarządzana przez _hosta_, który pełni rolę koordynatora - tworzy i obsługuje wiele
instancji klienta.

## Rozdział 2: Podstawy teoretyczne i stos technologiczny

## Rozdział 3: Opis studium przypadku

## Rozdział 4: Architektura rozwiązania

## Rozdział 5: Konfiguracja środowiska

## Rozdział 6: Sposób instalacji

## Rozdział 7: Etapy wdrażania demo

### Konfiguracja

### Przygotowanie danych

## Rozdział 8: Opis demo

### Procedura wykonania

### Wyniki

## Rozdział 9: Podsumowanie i wnioski

## Rozdział 10: Referencje
