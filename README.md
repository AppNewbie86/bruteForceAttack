# bruteForceAttack
![key](https://github.com/AppNewbie86/bruteForceAttack/assets/101304191/a8097b82-ef06-4e30-9b34-6fe602af538c)

# Brute-Force-Angriffsdetektor

Dies ist ein Python-Programm, das entwickelt wurde, um einen Brute-Force-Angriff auf eine Webseite zu erkennen und darauf zu reagieren.

Projektlaufzeit : 3 Monate

## Funktionen

### `brute_force_attack(url, username, password_list, rate_limit, two_factor_auth, password_manager)`

Führt einen Brute-Force-Angriff auf eine Webseite durch, um das Passwort für einen bestimmten Benutzer zu ermitteln.

- `url`: Die URL der Login-Seite.
- `username`: Der Benutzername, für den das Passwort gesucht wird.
- `password_list`: Eine Liste von Passwörtern, die ausprobiert werden.
- `rate_limit`: Die maximale Anzahl von Anfragen pro Sekunde, um eine Rate-Begrenzung zu verhindern.
- `two_factor_auth`: True, wenn die Webseite eine Zwei-Faktor-Authentifizierung erfordert, sonst False.
- `password_manager`: True, wenn ein Passwort-Manager verwendet werden soll, um Passwörter abzurufen, sonst False.

### `check_rate_limit(url)`

Überprüft, ob die Rate-Begrenzung auf der Webseite erreicht wurde.

- `url`: Die URL der Rate-Begrenzung-Seite.
- Rückgabewert: True, wenn die Rate-Begrenzung erreicht wurde, sonst False.

### `sleep_until_rate_limit_reset(url)`

Wartet, bis die Rate-Begrenzung aufgehoben ist, indem die Zeit bis zum Zurücksetzen der Rate-Begrenzung abgewartet wird.

- `url`: Die URL der Rate-Begrenzung-Seite.

### `generate_two_factor_code()`

Generiert einen Zwei-Faktor-Authentifizierungscode. Diese Methode sollte entsprechend den Anforderungen der Webseite implementiert werden.

### `get_password_from_password_manager(username, password)`

Ruft das Passwort aus dem Passwort-Manager ab.

- `username`: Der Benutzername.
- `password`: Das ursprüngliche Passwort, das aus dem Passwort-Manager abgerufen werden kann.

## Verwendung

Um den Brute-Force-Angriffsdetektor zu verwenden, rufen Sie die `brute_force_attack`-Funktion in Ihrer Python-Anwendung auf. Stellen Sie sicher, dass Sie die erforderlichen Parameter bereitstellen, um den Angriff zu konfigurieren.

```python
url = "https://example.com/login"
username = "admin"
password_list = ["password1", "password2", "password3"]
rate_limit = 10
two_factor_auth = True
password_manager = True

brute_force_attack(url, username, password_list, rate_limit, two_factor_auth, password_manager)

