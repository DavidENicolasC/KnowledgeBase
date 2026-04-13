When you reference a missing attribute (e.g., {does-not-exist}), the AsciiDoc processor will leave the attribute reference behind.

If you undefine an attribute on the same line as other text (e.g., {set:attribute-no-more!}), the processor will drop the whole line.

You can tailor these behaviors using the [[attribute-missing]] and [[attribute-undefined]] attributes.