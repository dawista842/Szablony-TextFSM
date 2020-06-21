# Szablony-Textfsm
Szablony TextFSM do urządzeń firmy Raisecom i DCN. Każdy szablon składa się ze zmiennych wyszczególnionych na początku pliku. Te same nazwy można również wyświetlić z poziomu skryptu Python:

```python
templateObject = textfsm.TextFSM(templateFile)
parsedText = templateObject.ParseText(textToParse)
print(templateObject.header)
```

Output na przykładzie komendy "show ip-access-list":

```
['LIST_NUMBER', 'ACCESS', 'PROTOCOL', 'REF', 'SOURCE', 'DESTINATION']
```

&nbsp;
## Konwersja sparsowanego teksu z tablicy do słownika

Aby sparsowany wynik przekształcić na formę słownika (tablica par "klucz - wartość") należy posłużyć się linijką:

```python
parsedCollection = [dict(zip(templateObject.header, item)) for item in parsedText]
```
