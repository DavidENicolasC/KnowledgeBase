Fixed set of recognized block enclosures in the [[AsciiDoc]] syntax, known as [[Linewise delimiters]].

Has an expected [[Content model]]. [[Context]] is default when an explicit [[Block style]] is not present.

The types are the following:

| Type    | Default [[Context]] | Expect [[Content Model]] | Minimum delimiter            |
| ------- | ------------------- | ------------------------ | ---------------------------- |
| comment | `n/a`               | `n/a`                    | ////                         |
| example | :example            | compound                 | `====`                       |
| listing | :listing            | verbatim                 | `----`                       |
| literal | :literal            | verbatim                 | `....`                       |
| open    | :open               | compound                 | `--`                         |
| sidebar | :sidebar            | compound                 | `****`                       |
| table   | :table              | table                    | `\|===`,`,===`,`:===`,`!===` |
| pass    | :pass               | raw                      | `++++`                       |
| quote   | :quote              | compound                 | `----`                       |

Comment is not preserved in the parsed document and doesn´t have a context or content model.

It's important to choose a structural container that provides the right [[Content model]].