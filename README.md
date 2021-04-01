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

In user entry, the space at character 4 might be significant. (ie. I typed "A1B" vs "A1B ")

Applied to a complete postal code, `.normalize` is equivalent to `.format`.

### .matchPrefix(string)
Returns an abbreviation of the province or territory, based on the first character (or 3 first).

```js
PostalCode.matchPrefix("G1A 1A1")
// "QC"
```

*Abbreviations follow [ISO 3166-2:CA][30].*

Data as a list of prefix–region pairs is available in [prefixes.json](prefixes.json) and in the public domain.

[30]: https://en.wikipedia.org/wiki/Canadian_postal_abbreviations_for_provinces_and_territories#Names_and_abbreviations
