Orygianlny plik był w formacie .csv, więc był on importowalny bez dodatkowych działań. 
Plik można wczytać w Pythonie przy pomocy funkcji z biblioteki pandas: read_csv(filename).

Oryginalne dane przetworzę w nowy plik o formacie .csv.
Skorzystam z języka Python i bibliotek Numpy oraz Pandas. 
Na początku utworzę dodatkową funkcję do ekstrakcji danych o płci i wieku z nazy kolumny. 
Następnie przygotowuje słownik, do którego będę przepisywał dane oryginalnego pliku.
Przepiszę wszystkie dane, organizując kolumny w inny sposób i pomijając puste komórki.
Szczegóły implementacji są w pliku data_processing.ipynb.
w pliku data_processing.ipynb znajduje się kod realizujący przetwarzanie danych oraz komentarze opsiujące kolejne kroki algorytmu.

Aby uzyskać wykresy i opisy przetworzonych danych napisałem skrypt data_appendix_maker.ipynb.
Po uruchomieniu pliku data_appendix_maker.ipynb informacje o danych oraz wykresy zostają zapisane do folderu Documents.

Struktura katalogów:

Tuberculosis_in_different_patient_groups: folder główny
	- Analysis_Data: zawiera przetworzony plik, gotowy do analizy
	- Command_Files: zawiera pliki: 
		* data_processing.ipynb, który przetwarza oryginalne dane i zapisuje je do folderu Analysis_Data
		* data_appendix_maker.ipynb, który analizuje dane w nowym formacie i zapisuje informacje do pliku data_appendix.txt
	- Original_Data: zawiera oryginalny plik tb.csv oraz folder Metadata:
		* Metadata: zawiera plik metadata_guide.txt z opisem oryginalnego pliku
	- Documents: zawiera plik README.md oraz data_appendix.txt oraz pliki graficzne z wykresami

Aby odtworzyć uzyskane wyniki:
	0. Potrzebujemy oprogramowania interpretującego Python 3 w postaci plików .ipynb, przykładowo Jupyter Notebook.
	1. Tworzymy strukturę katalogów taką jak jest opisana powyżej i kopiujemy plik z oryginalnymi danymi. 
	2. Ustawiamy główny folder projektu jako folder roboczy.
	3. Uruchamiamy jupyterowy plik data_processing (w którym importowane są potrzebne biblioteki: Numpy i Pandas).
	   Skrypt ten wczyta oryginalne dane z pliku .csv i dokona odpowiednich przekształceń, a następnie zapisze nową wersję.
	4. Uruchamiamy jupyterowy plik data_appendix_maker, który zawiera kod pozwalający na wstępną analizę danych.
	   Skrypt ten wczytuje przetworzony plik .csv.
	   Wynikiem programu jest plik data_appendix.txt zawierający opis zmiennych oraz pliki graficzne z podstawowymi
	   wykresami opisującymi dane.