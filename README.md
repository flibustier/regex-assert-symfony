# Regex-Assert-Symfony
Commun Regex to use with Assert in Symfony's entity

## Email

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

