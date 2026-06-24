Those are the rules on how a composite gets created:

- `string`: stays the same for the resulting header value
- `array`: items are joined by `,` for the resulting header value
- `key-value`: items are composed from: key + space + value. Items are then joined by `;` for the resulting header value
- `null`: header will be ignored