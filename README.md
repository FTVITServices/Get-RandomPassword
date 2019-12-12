# Get-RandomPassword
Generates random passwords using random common words

[Test your password here!](https://howsecureismypassword.net/)

Based on https://xkcd.com/936/ and https://xkpasswd.net/s/

Words provided by https://github.com/first20hours/google-10000-english



## How to use it
Running `Get-Help .\Get-RandomPassword` will provide some details and examples, but here's a description of each parameter and what they do

Parameters | Functionnality
-----------|-------
Words | Number of words that the password will contain. The default is 3. Example: "car-HORSE-staple" is a 3 word password
Delimiter | Separator for the passwords. Default is a dash (-). Example: "car!HORSE!staple" the delimiter here would be the exclamation point (!)
Count | Number of passwords you want generated. Default is 3.
Short | Generates a password containing short words (1-4 characters long).
Medium | Generates a password containing medium words (5-8 characters long) (default if no length is specified)
Long | Generates a password containing long words (9+ characters long)
NoCapitalization | Specifies that all words will be in lowercase
DoNotCopyToClipboard | Will not copy a random password to your clipboard

**Please note that only one word length can be specified**

## Examples

```powershell
# This example generates 3 passwords containing 3 words each
.\Get-RandomPassword
studying-LODGE-ECLIPSE
CONGO-whilst-YOURS
COOLING-ELECTRO-BOXING
```

```powershell
# This example generates 3 passwords with 5 words per password.
# The Sun would die before a computer could crack these passwords
# It uses the default delimiter "-" (a dash) and a medium dictionnary (5-8 characters long)
.\Get-RandomPassword -Word 5
MAGICAL-TOWARDS-reunion-burke-PERFUME
DEEPLY-JOHNNY-MICHELLE-official-BRUSH
knives-PLANT-divine-warcraft-minister
```

```powershell
# This example generates 5 passwords containing 4 words each with the asterisk delimiter
# The -Long switch was specified, therefore it used words that are over 9 characters long
.\Get-RandomPassword -Word 4 -Count 5 -Delimiter * -Long
QUESTIONNAIRE*deutschland*UNDEFINED*VIEWPICTURE
SMITHSONIAN*BURLINGTON*independent*PARTNERSHIPS
COUNSELING*subsequently*CHRISTINA*associations
JURISDICTION*WEBMASTERS*FILTERING*conditions
PROVIDING*RESIDENTS*ACDBENTITY*CORRECTION
```

```powershell
# This example generates 4 passwords with 5 words each
# The -Short switch was specified, therefore it uses words that are in between 1 and 4 characters long
.\Get-RandomPassword -Word 5 -Count 4 -Short
rats-leon-POEM-ks-OVEN
DAM-bull-BABY-ICT-hey
news-teen-ace-PHIL-ba
bank-SEO-NAM-PREV-NM
```

