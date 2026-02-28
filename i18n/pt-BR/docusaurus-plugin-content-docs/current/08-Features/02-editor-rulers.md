# Réguas do Editor

Adicione réguas de coluna verticais ao editor para acompanhar o comprimento das linhas. Por padrão, uma única régua é definida na posição de 120 caracteres.

### Habilitando e Desabilitando Réguas

Alterne a visibilidade das réguas através da opção de menu `Ver > Réguas`.

![Captura de tela das réguas](https://private-user-images.githubusercontent.com/5336369/326161983-bb68fafa-395c-4da6-8aa2-a617918286ce.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NzIyNTQ3MzIsIm5iZiI6MTc3MjI1NDQzMiwicGF0aCI6Ii81MzM2MzY5LzMyNjE2MTk4My1iYjY4ZmFmYS0zOTVjLTRkYTYtOGFhMi1hNjE3OTE4Mjg2Y2UucG5nP1gtQW16LUFsZ29yaXRobT1BV1M0LUhNQUMtU0hBMjU2JlgtQW16LUNyZWRlbnRpYWw9QUtJQVZDT0RZTFNBNTNQUUs0WkElMkYyMDI2MDIyOCUyRnVzLWVhc3QtMSUyRnMzJTJGYXdzNF9yZXF1ZXN0JlgtQW16LURhdGU9MjAyNjAyMjhUMDQ1MzUyWiZYLUFtei1FeHBpcmVzPTMwMCZYLUFtei1TaWduYXR1cmU9ZDIzM2M3ODI1NTMwZWQ1NDhkZmVjNzJlYzkzYWI5ZWRmZjMzMzU0N2Y4MDY5MzlhYzVlNTE3YzE4ZTJhZGVkZiZYLUFtei1TaWduZWRIZWFkZXJzPWhvc3QifQ.qBruRgYTwUX5e326v3Tg3-tVka3QwGS8ZyWabjA6SCU)

## Adicionando Múltiplas Réguas

Para adicionar múltiplas réguas, edite o arquivo de preferências:

1. Navegue até `Arquivo > Abrir Arquivo de Preferências`.
2. Adicione as seguintes entradas à configuração JSON:

```json
{
  // itens json existentes
  "editor.rulers": [40, 80],
  "editor.rulerColors": ["green", "#f34d5a"]
}
```

Essas configurações introduzem duas réguas nas posições dos caracteres 40 e 80, coloridas de verde e vermelho, respectivamente.

![imagem](https://private-user-images.githubusercontent.com/5336369/326161588-71b8b04c-d2ca-47b8-84bb-53cd0fb4593c.png?jwt=eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJpc3MiOiJnaXRodWIuY29tIiwiYXVkIjoicmF3LmdpdGh1YnVzZXJjb250ZW50LmNvbSIsImtleSI6ImtleTUiLCJleHAiOjE3NzIyNTQ3MzIsIm5iZiI6MTc3MjI1NDQzMiwicGF0aCI6Ii81MzM2MzY5LzMyNjE2MTU4OC03MWI4YjA0Yy1kMmNhLTQ3YjgtODRiYi01M2NkMGZiNDU5M2MucG5nP1gtQW16LUFsZ29yaXRobT1BV1M0LUhNQUMtU0hBMjU2JlgtQW16LUNyZWRlbnRpYWw9QUtJQVZDT0RZTFNBNTNQUUs0WkElMkYyMDI2MDIyOCUyRnVzLWVhc3QtMSUyRnMzJTJGYXdzNF9yZXF1ZXN0JlgtQW16LURhdGU9MjAyNjAyMjhUMDQ1MzUyWiZYLUFtei1FeHBpcmVzPTMwMCZYLUFtei1TaWduYXR1cmU9YTIyNzYwZjZlZDZjOWZmZTdhZmQ4ZGUyNmQzODk2NTEwMjhkZmM1MGEwYWI1OWQ0MjJmNTk2YTRjNjA5NGNkYSZYLUFtei1TaWduZWRIZWFkZXJzPWhvc3QifQ.dLnf5FqcSFyqe71XIZDxvlTE7Ji-KnJeii_0ZiqSOp0)

#### Opções de Configuração

1. `editor.rulers`: Especifica uma matriz de números de coluna onde as réguas verticais aparecerão.
2. `editor.rulerColors`: Uma matriz opcional para definir cores para cada régua, correspondendo às posições listadas em `editor.rulers`.

## FAQ

#### P: Como adiciono réguas diferentes para cada projeto?

Para configurar réguas diferentes para projetos individuais, crie um arquivo `.phcode.json` no diretório raiz de cada projeto. Inclua as mesmas configurações de régua mostradas no exemplo acima.
