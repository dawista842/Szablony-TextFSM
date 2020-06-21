# Szablony-Textfsm
Szablony TextFSM do urządzeń firmy Raisecom i DCN. Każdy szablon składa się ze zmiennych wyszczególnionych na początku pliku. Te same nazwy można również wyświetlić z poziomu skryptu Python:

```python
templateObject = textfsm.TextFSM(templateFile)
parsedText = templateObject.ParseText(textToParse)
print(templateObject.header)
```
