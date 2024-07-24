# Beta testy KF2.0

Testowa wersja gry jest wystawiona pod adresem [beta.kf2.pl](https://beta.kf2.pl)

# Podstawowe funkcjonalności do przejrzenia

**Kreator postaci**: przełączanie między podstronami, wybór opcji kreatora, podanie imienia (można przetestować walidację różnych znaków).

**Lobby**: wybór postaci, przełączanie między postaciami w różnych zakładkach przeglądarki. Niezależnie od zakładki zawsze powinna być wybrana jedna postać.

**Gildie**: Zakładanie gildii, usuwanie gildii, nadawanie uprawnień, wpłacanie złota do skarbca. W przypadku zakładania, czy usuwania gildii trzeba sprawdzić czy dane o gildii na liście graczy online aktualizują się poprawnie. W przypadku wielu otwartych zakładek także warto to sprawdzić.

**HexMapa**: Dołączanie na mapę, poruszanie się po mapie, mapowanie, teleportacja między miastami, zakładanie siedziby gildii. Przy czym najważniejsze tutaj jest przetestowanie tego na jak największej liczbie urządzeń, w wielu zakładkach, także przy słabszych i starszych urządzeniach. 

## Dodatkowe informacje

System jest zbudowany tak  by nie przeładowywać strony dzięki czemu przełączanie się między podstronami przebiega szybko. Komunikacja z serwerem jest dwukierunkowa to znaczy, że użytkownik może otrzymywać informacje z serwera nawet jeśli o nie nie wysłał requestu. Lista eventów, które mogą pomóc w głębszym testowaniu:

**client.character** - aktualizuje dane aktualnie wybranej przez użytkownika postaci.
**client.character.list** - aktualizuje dane na liście użytkowników online, tutaj są dwa pokoje do których są wysłane dane:
- Do wszystkich połączonych użytkowników (w każdym przypadku prócz poniższego)
- Do jednego gracza (otrzymuje listę graczy po wybraniu postaci).
**client.map.update** - aktualizuje dane mapy, oraz pionka na mapie, jest wysyłany przy wszystkich akcjach na mapie.

Więcej informacji pojawi się wraz z kolejnymi funkcjonalnościami.
