# Regex-Assert-Symfony
Commun Regex to use with Assert in Symfony's entity

## Firstname Lastname City
Compatible with international names

### Pattern
```
/^[a-zA-ZàáâäãåąčćęèéêëėįìíîïłńòóôöõøùÞúûüųūæÿýżźñçčšžÀÁÂÄÃÅĄĆČĖĘÈÉÊËÌÍÎÏĮŁŃÒÓÔÖÕØÙÚÛÜŲŪŸÝŻŹÑßÇŒÆČŠŽ∂ð ,.'-]+$/u
```

### Usage
```
@Assert\Regex(pattern="/^[a-zA-ZàáâäãåąčćęèéêëėįìíîïłńòóôöõøùæúûüųūÿýżźñçÞčšžÀÁÂÄÃÅĄĆČĖĘÈÉÊËÌÍÎÏĮŁŃÒÓÔÖÕØÙÚÛÜŲŪŸÝŻŹÑßÇŒÆČŠŽ∂ð ,.'-]+$/u")
```

### Lastname Firstname Examples

    Mathias d'Arras
    Martin Luther King, Jr.
    Hector Sausage-Hausen

### City Examples

    Toronto
    St. Catharines
    San Fransisco
    Val-d'Or
    Presqu'ile
    Niagara on the Lake
    Niagara-on-the-Lake
    München
    toronto
    toRonTo
    villes du Québec
    Provence-Alpes-Côte d'Azur
    Île-de-France
    Kópavogur
    Garðabær
    Sauðárkrókur
    Þorlákshöfn

## Postal code
Compatible with international country code

### Pattern
```
/^[0-9 ,.-]+$/
```

### Usage
```
@Assert\Regex(pattern="/^[0-9 ,.-]+$/")
```

### Examples

    1234
    69001
    12-3456
    1234-5678
    
## Email
It's recomended to use the string constraints [Email](http://symfony.com/doc/current/reference/constraints/Email.html)

### Usage
```
/**
 * @Assert\Email(
 *     message = "The email '{{ value }}' is not a valid email.",
 *     checkMX = true
 * )
 */
```
