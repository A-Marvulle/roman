# Roman Numeral Converter

<h2>Exercise</h2>
<p>Convert the given number into a roman numeral.</p>

<table>
  <tr>
    <th>Roman numerals</th>
    <th>Arabic numerals</th>
  </tr>
  <tr>
    <th>M</th>
    <th>1000</th>
  </tr>
  <tr>
    <th>CM</th>
    <th>900</th>
  </tr>
  <tr>
    <th>D</th>
    <th>500</th>
  </tr>
  <tr>
    <th>CD</th>
    <th>400</th>
  </tr>
  <tr>
    <th>C</th>
    <th>100</th>
  </tr>
  <tr>
    <th>XC</th>
    <th>90</th>
  </tr>
  <tr>
    <th>L</th>
    <th>50</th>
  </tr>
  <tr>
    <th>XL</th>
    <th>40</th>
  </tr>
  <tr>
    <th>X</th>
    <th>10</th>
  </tr>
  <tr>
    <th>IX</th>
    <th>9</th>
  </tr>
  <tr>
    <th>V</th>
    <th>5</th>
  </tr>
  <tr>
    <th>IV</th>
    <th>4</th>
  </tr>
  <tr>
    <th>I</th>
    <th>1</th>
  </tr>
</table>

<p>All roman numerals answers should be provided in upper-case.</p>

<h2>Code</h2>

```
function convertToRoman(num) {
let numOg = num;
  if (num <= 0 || num > 3999) {
    return "Invalid number. Please enter a number between 1 and 3999.";
  }

  const romanNumerals = [
    { value: 1000, numeral: 'M' },
    { value: 900, numeral: 'CM' },
    { value: 500, numeral: 'D' },
    { value: 400, numeral: 'CD' },
    { value: 100, numeral: 'C' },
    { value: 90, numeral: 'XC' },
    { value: 50, numeral: 'L' },
    { value: 40, numeral: 'XL' },
    { value: 10, numeral: 'X' },
    { value: 9, numeral: 'IX' },
    { value: 5, numeral: 'V' },
    { value: 4, numeral: 'IV' },
    { value: 1, numeral: 'I' }
  ];

  let result = '';

  for (const numeral of romanNumerals) {
    while (num >= numeral.value) {
      result += numeral.numeral;
      num -= numeral.value;
    }
  }

  return console.log("================\nConversor Romano\n================\nOriginal: "+numOg + "\nResultado: " + result);
}
```

<h2>Exemple</h2>

```
convertToRoman(52);

================
Conversor Romano
================
Original: 52
Resultado: LII
```
<a href="" target=_blank>Pages</a>
