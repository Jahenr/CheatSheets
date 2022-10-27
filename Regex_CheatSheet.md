Regex:
    # Character Class

    [xyz]
    [a-c]

    # Meaning

    A character class. Matches any one of the enclosed characters. You can specify a range of characters by using a hyphen, but if the hyphen appears as the first or last character enclosed in the square brackets, it is taken as a literal hyphen to be included in the character class as a normal character.

    For example, [abcd] is the same as [a-d]. They match the "b" in "brisket", and the "a" or the "c" in "arch", but not the "-" (hyphen) in "non-profit".

    For example, [abcd-] and [-abcd] match the "b" in "brisket", the "a" or the "c" in "arch", and the "-" (hyphen) in "non-profit".

    For example, [\w-] is the same as [A-Za-z0-9_-]. They both match any of the characters in "no_reply@example-server.com" except for the "@" and the ".".

    # Negated or Complemented Character Class

    [^xyz]
    [^a-c]

    # Meaning

    A negated or complemented character class. That is, it matches anything that is not enclosed in the brackets. You can specify a range of characters by using a hyphen, but if the hyphen appears as the first or last character enclosed in the square brackets, it is taken as a literal hyphen to be included in the character class as a normal character. For example, [^abc] is the same as [^a-c]. They initially match "o" in "bacon" and "h" in "chop".

    # Note: ^ May also indicate the beginning of input

    # Character

    [.]

    # Meaning

    Has one of the following meanings:

    Matches any single character except line terminators: \n, \r, \u2028 or \u2029. For example, /.y/ matches "my" and "ay", but not "yes", in "yes make my day".

    Inside a character class, the dot loses its special meaning and matches a literal dot.
    Note that the m multiline flag doesn't change the dot behavior. So to match a pattern across multiple lines, the character class [^] can be used — it will match any character including newlines.

    The s "dotAll" flag allows the dot to also match line terminators.

    # Character

    [\d]

    # Meaning

    Matches any digit (Arabic numeral). Equivalent to [0-9]. For example, /\d/ or /[0-9]/ matches "2" in "B2 is the suite number".

    # Character

    [\D]

    # Meaning

    Matches any character that is not a digit (Arabic numeral). Equivalent to [^0-9]. For example, /\D/ or /[^0-9]/ matches "B" in "B2 is the suite number".

