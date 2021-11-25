Tworzenie oprogr. dla sys. chmur. (w), dr Paweł Fałat, 18.09.2021

TOdsC_wyk_2021-09-18

# Wykład 1

## Zaliczenie wykładu
- Przygotowanie 10 min. prezentacji na tematy związ. z chmurą, do pokazania.

## Zaliczenie lab.
- Mgr Rudyk.

## Chmura
- HAS - hardware as a service - korzysta się ze sprzętu, samodzielnie się stawia system.
- SAS - software as a service - w chmurze jest gotowe oprogr., np. Gmail, Ms Office online
- PAS - platform as a service - apki wdrażamy sami, ale system już jest.

## Azure
- dostarcza usłubi obliczeniowe przez Internet: serwery, magazyn plików, bazy danych, oprogr., analizy, sztuczna intelig., uczenie maszyn.
- pozwala obniżyć koszty, ułatwia uruchamianie infrastruktury, skalowanie i dopasowanie do potrzeb

## Azure Portal interfejs
- tworzenie i monitorowanie aplikacji internetowych, wdrożenia i zarządzanie
- tworzenie customowych puplitów nawigacyjnych 
- optymalizacja środowiska 

## Usługi Azure
- obliczeniowe: Azure Virtual Machines, Azure Virtual Machine Scale Sets, Azure Kubernetes Service...
- sieciowe: Azure Virtual Network, Azure Load Balancer, Azure DDoS Protection (denial of service)...
- magazynowe: Azure Blob Storage, Azure File Storage
- mobilne
- IoT: IoT Central, Azure IoT Hub...
- internetowe: Azure App Service...
- bazy danych: MySql, PostreSQL, Azure SQL...
- DevOps
- AI (Azure Machine Learing Service)

## Subskrypcje Azure
- darmowa
-- bezpłatny dostęp do popularnych produktów platformy Azure przez 12 mies.
-- środki do wydania przez pierwsze 30 dni
-- dostęp do 25 bezpłatnych produktów

- studencka
-- https://azureforeducation.microsoft.com/devtools
-- bezpłatny dostęp do niektórych usług platformy Azure przez 12 mies.
-- kredyt $100 do użycia w ciągu pierwszych 12 mies.
-- bezpłatny dostęp do niektórych narzędzi dla programistó

- developerska
-- https://visualstudio.microsoft.com/pl/dev-essentials/
-- sprawdzić, bo chyba już nie ma
-- było 300$ na 6 lub 12 mies.

## Dodatkowe subskrypcje Azure
- konto Azure account:
	- subskrypcje
		- resource groups
			- resources
- konto rozliczeniowe:
	- profil rozliczeniowy
		- sekcje faktur
			- subskrypcje

## Piaskownica środowiska Learn
- tymczasowa subskrypcja dodawana do konta platformy Azure
- umożliwia tworzenie zasobów Azure na czas szkolenia
- czyszczone po zakończeniu szkolenia

## Rejestracja
- wersja studencka wymaga konta w edu.pl
- opcja uruchamienia środków
- materiały szkoleniowe pod Informacje

## Maszyny wirtualne
- usługa typu IaaS (infrastructure as a service)
- co konfiguralne: procesor, RAM, dysk, limity kart sieciowych
- podział:
-- Basic tier: tańsze, do 8 rdzeni proc., 14 GB pamięci i maks. 16 dysków danych, użycia nieprod., bez skalowania automatycznego, duża dostępność (tańsze)
-- Standard tier: produkcyjne
- inny podział: ogólnego przeznaczenia, do obliczeń poufnkych, zoptymalizowana pod kątem obliczeń, pamięci, magazynowania, wydajności obliczeń
- dyski
-- systemu operacyjnego: zawsze 1, maks. 2 TB, C:\
-- danych: maks. 32TB, typu SSD lub HDD
-- tymczasowe: 1 na plik stronicowania, cache
- dyski mogą być zarządzane i niezarządzane

## Skalowanie maszyn wirtualnych
- usługa Azure Batch
-- uruchamia pulę obliczeniowych maszyn wirt.
-- obsługuje błędy

## Container Instances i Azure Kubernetes Service
- wdrażanie kontenerów

## Azure App Services
- PaaS (Platform as a Service)
- szybkie tworzenie i wdrażanie apek internetowych, mobilnych, API
- apki internetowe ASP.NET, ASP.NET Core, Java, Ruby, Node.js, PHP, Python
- bez zarządzania infrastrukturą 

## Wdrażanie
- witryna Azure Portal (interfejs graficzny)
- Azure PowerShell lub interfejs wiersza polecenia platformy Azure: skrypty, obrazy niestandardowe
- szablony usługi Azure Resource Manager (duże wdrożenia)
- Windows Admin Center (nietypowe obrazy, migracje itp.)
- zob. filmik create virtual machine
- z wiersza poleceń

------

## Kod do grupy na Teamsach

`e3r8918`

------



















