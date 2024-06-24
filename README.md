# easyeda-converter

> [!WARNING]
> This library is a work in progress! Not everything works yet!

Convert easyeda JSON PCB footprints into [tscircuit json soup](https://docs.tscircuit.com/api-reference/advanced/soup)

## Library Usage

```ts

```

## CLI

Install the CLI with `npm install -g easyeda-converter`

**The CLI is interactive, just run `easyeda-converter` to
start the interactive prompt.**

```sh
# Convert a schematic and footprint for JLCPCB part number C46749 (NE555) to tscircuit component
easyeda-converter convert -i C46749 -o C46749.ts

# Convert a footprint and schematic for JLCPCB part number C46749 (NE555) to tscircuit soup JSON
# More info: https://docs.tscircuit.com/api-reference/advanced/soup
easyeda-converter convert -i C46749 -o C46749.soup.json

# Convert a footprint for JLCPCB part number C46749 (NE555) to KiCad footprint
easyeda-converter convert -i C46749 -o C46749.kicad_mod

# Download the C46749 footprint and schematic and convert to readable JSON
easyeda-converter convert -i C46749 -o C46749.bettereasy.json

# Can also convert from files!
easyeda-converter convert -i ./C46749.raweasy.json -o C46749.soup.json

# Get exactly what is returned from the JLC API
# The footprint, schematic and some other data is encoded in strings, you
# probably want to convert to *.bettereasy.json
easyeda-converter download -i C46749 -o C46749.raweasy.json
```
