# SmartStacker: Integracja TIA Portal z Factory IO dla Zautomatyzowanych Systemów Produkcyjnych

## O Projekcie

SmartStacker to edukacyjny projekt do symulacji i kontroli zautomatyzowanej linii produkcyjnej. Projekt skupia się na nauczaniu programowania PLC poprzez praktyczne doświadczenie ze środowiskiem TIA Portal wraz z symulatorem sterownika.

## Cele Projektu

- **Edukacja:**  nauka programowania PLC na programie symulacyjnym i zrozumienia jego aplikacji w realnych scenariuszach przemysłowych.
- **Symulacja:** Demonstracja możliwości symulacji zautomatyzowanej linii produkcyjnej, w tym sortowania i wykrywania  produktów.

## Technologie i Narzędzia

Projekt wykorzystuje następujące technologie i narzędzia:
- TIA Portal
- Factory IO
- Simatic S7 PLCSIM S7-1200

## Funkcjonalność i Opis Działania 
Składa się ona z dwóch głównych taśmociągów, na których umieszczono dwa stanowiska montażowe do składania pudełek. Każde z tych stanowisk wyposażone jest w:
- Robot Montażowy
- Bramę Przesuwną
- Siłownik Wyrównujący Pudełka
- Czujniki Położenia
- Kamera Wizyjna

## Sekwencje Sterowania
### Sekwencje Pokryw
- `Sequence_lids_at_place` - Wskazuje, czy pokrywy znajdują się na wyznaczonym miejscu.
- `Sequence_lids_is_fitted` - Określa, czy pokrywy zostały właściwie dopasowane.
- `Sequence_lids_is_grabbed` - Monitoruje, czy pokrywy zostały chwyczone przez roboty montażowe.
- `Sequence_lids_above_base` - Sygnalizuje, że pokrywy znajdują się bezpośrednio nad podstawami.

### Sekwencje Podstaw
- `Sequence_bases_at_place` - Wskazuje, czy podstawy są na swoich miejscach w strefie montażu.
- `Sequence_bases_is_fitted` - Określa, czy podstawy zostały prawidłowo zamontowane.

### Sekwencje Części
- `Sequence_part_is_stacked` - Sygnalizuje, że części zostały poprawnie ułożone w stos.
- `Sequence_part_above_lids` - Wskazuje, czy części znajdują się nad pokrywami.
- `Sequence_part_at_place` - Monitoruje, czy części znajdują się na wyznaczonym miejscu.
- `Sequence_part_exit` - Informuje, że część opuściła strefę montażową.

### Sekwencje Braku Niebieskich Elementów
- `Sequence_no_blue_lids` - Określa, czy w procesie nie występują niebieskie pokrywy.
- `Sequence_no_blue_bases` - Sygnalizuje brak niebieskich podstaw w procesie.
- 
### Wykorzystanie funkcji Fb do 2 stanowisk 
Blok DB1 jest przypisyany do 1 stanowiska , Blok DB2 do drugiego

## Demo Wideo

[![Demo Video1]()](project_box_stacking/videos/demo_video.mp4)
[![Demo Video2]()](project_box_stacking/videos/demo_video.mp4)

## Drzewo Projektu , Main OB1
![](project_box_stacking/images/main_view.PNG)

## Main OB1 networks
![](project_box_stacking/images/OB1_net1-net2.PNG)
![](project_box_stacking/images/OB1_net3.PNG)
![](project_box_stacking/images/OB1_net4.PNG)
![](project_box_stacking/images/OB1_net5.PNG)

## Main FB1 networks 
![](project_box_stacking/images/FB_networks.PNG)
![](project_box_stacking/images/FB_variables.PNG)
![](project_box_stacking/images/FB1_variables_2.PNG)
![](project_box_stacking/images/FB1_net1.PNG)
![](project_box_stacking/images/FB1_net2-5.PNG)
![](project_box_stacking/images/FB1-net5-7.PNG)
![](project_box_stacking/images/FB1-net8-10.PNG)
![](project_box_stacking/images/FB1-net11-13.PNG)
![](project_box_stacking/images/FB1-net14-17.PNG)
![](project_box_stacking/images/FB1-net18-20.PNG)
![](project_box_stacking/images/FB1-net21-23.PNG)
![](project_box_stacking/images/FB1-net24.PNG)

### DB1 watch table
![DB1 Variables](project_box_stacking/images/watch_table_DB1.PNG)

### DB2 watch table
![DB2 Variables](project_box_stacking/images/watch_table_DB2.PNG)

## FC system on/off
![FC1 Network 1](project_box_stacking/images/FC1-net1.PNG)

### PLC Tags
![PLC Tags](project_box_stacking/images/Tag_table_FactoryIO_1.PNG)
![PLC Tags](project_box_stacking/images/Tag_table_FactoryIO_2.PNG)
![PLC Tags](project_box_stacking/images/Tag_table_on_off.PNG)
![PLC Tags](project_box_stacking/images/PLC_tags_standardvariable_tabelle.PNG)



