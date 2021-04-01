# postal-code.canada.js

A \[work in progress for a\] small postal code library.

## Usage

### .isValid(string)
```js
PostalCode.valid?("F8G 1A1") 
// false
```

### .normalize(string)
The standard format being `A0A 0A0`. (capital letters, one space)

```js
PostalCode.normalize("e3b.4k5 ") 
// "E3B 4K5"
```

### .format(string)
Formats a postal code string, even if it is partial (eg: when typing). 

```js
PostalCode.format("j1k4") 
// "J1K 4"
```

Applied to a complete postal code, `.normalize` is equivalent to `.format`.

### .guessRegion(string)
Returns an abbreviation of the province or territory, based on the first character (or 2 first).

```js
PostalCode.guessRegion("G1A 1A1")
// "QC"
```

*Abbreviations follow [ISO 3166-2:CA][30].*

[30]: https://en.wikipedia.org/wiki/Canadian_postal_abbreviations_for_provinces_and_territories#Names_and_abbreviations
