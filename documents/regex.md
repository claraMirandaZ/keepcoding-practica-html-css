According to the form validation messages on Join Github page,
- Github username may only contain alphanumeric characters or hyphens.
- Github username cannot have multiple consecutive hyphens.
- Github username cannot begin or end with a hyphen.
- Maximum is 39 characters.

^(?=.{1,38}$)(?![_.])(?!.*[_.]{2})[a-zA-Z0-9._]+(?<![_.])$
 └─────┬────┘└───┬──┘└─────┬─────┘└─────┬─────┘ └───┬───┘
       │         │         │            │           no _ or . at the end
       │         │         │            │
       │         │         │            allowed characters
       │         │         │
       │         │         no __ or _. or ._ or .. inside
       │         │
       │         no _ or . at the beginning
       │
       username is 1-38 characters long

/^@(?=[a-zA-Z0-9._]{1,38}$)(?!.*[_.]{2})[^_.].*[^_.]$/

<!-- https://projects.lukehaas.me/regexhub/ -->