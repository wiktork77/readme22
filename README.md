# Projekt Social Tripper
Głównym celem projektu było opracowanie nowoczesnego portalu społecznościowego, który integruje funkcje organizowania podróży oraz dzielenia się relacjami z wyjazdów. Portal ten łączy cechy aplikacji typu social media z narzędziami przeznaczonymi do planowania i realizacji podróży. Projekt obejmował stworzenie dwóch aplikacji – mobilnej i webowej – współpracujących z bazami danych, w których przechowywane są informacje o użytkownikach, wydarzeniach oraz materiałach multimedialnych.
System został zaprojektowany z myślą o wspieraniu użytkowników w aktywnym udziale w podróżach oraz budowaniu społeczności wokół wspólnych pasji. System oferuje system rekomendacji, który na podstawie analizy preferencji użytkowników sugeruje interesujące wyjazdy oraz osoby o podobnych zainteresowaniach. Dzięki temu użytkownicy mogą w prosty sposób nawiązywać kontakty i planować wyjazdy zgodnie ze swoimi upodobaniami.

# Social Tripper Mobile 
Repozytorium zawiera kod aplikacji mobilnej projektu Social Tripper, która dostępna jest na androida.
Aplikacja mobilna jest dodatkiem do portalu społecznościowego, który jest w pełni zrealizowany za pomocą strony internetowej, aplikacja mobilna zawiera podzbiór funkcjonalności strony internetowej jeśli chodzi o typowe funkcjonalności social media, mobilke wyróżnia to, że możemy za pomocą aplikacji rozpocząć wyprawę i wrzucać zdjęcia, filmiki, które są przypisywane do konkretnych lokalizacji ich wykonania na ścieżce, jak i taką wyprawę możemy zakończyć, czego produktem jest "Relacja" - jest to podsumowanie wyprawy w postaci udostępnionej przebytej ścieżki, multimedialnych pinezek oraz slidera multimediów.
Inne funkcjonalności to przeglądanie postów, wypraw, aplikowanie do wypraw oraz przeglądanie mapy, no i login oraz rejestracja, które zrealizowane są za pomocą AWS Amplify.

# Plik Apk aplikacji
Ostateczna wersja aplikacji została zbudowana i udostępniona na publicznym repozytorium, tak, aby można było ją przetestować bez konieczności manualnej kompilacji, plik apk znajduje się pod linkiem: https://apkfab.com/socialtrippermobile/com.example.social_tripper_mobile/apk?h=4cdd19b24d161b30b1885665a9ade39317a36015470e0fa306bbbec5a185225c


# Instrukcja kompilacji
Najlepiej projekt uruchomić w Android Studio (wersja Koala), następnie przejść przez następującą procedurę wykonania kodu
## Kompilacja do wersji debug:
flutter clean
flutter pub get
flutter run
## Kompilacja do wersji release:
flutter clean
flutter pub get
flutter run --release

## Komponenty zależne
Do kompilacji potrzebne są następujące komponenty
- skonfigurowana usługa AWS Amplify: https://docs.amplify.aws/gen1/flutter/start/project-setup/prerequisites/
- uruchomiony backend, kod aplikacji backendowej znajduje się w następującym repozytorium: https://github.com/Lehito15/SocialTripper_Backend
- uruchomiony serwer WebSocket, kod serwera WebSocket znajduje się w następującym repozytorium: https://github.com/betonowylukasz/SocialTripper_WebSocket

## Odnośniki w kodzie
Aby podpiąć aplikację do backendu, który działa pod pewnym adresem, należy zmodyfikować plik lib\Pages\config\data_retrieving_config.dart oraz ustawić atrybut sourceUrl klasy DataRetrievingConfig na odpowiedni adres, wszystkie serwisy wykonują zapytania korzystając z tego punktu odniesienia
Aby podpiąć aplikację do serwera WebSocket, należy w pliku lib\Pages\trip_interface.dart zmienić atrybuty fileServerAddress oraz client, tak, aby odpowiadały nowemu adresowi






