# lijsten

## list-style-type

```css
ul.a {
  list-style-type: circle;}
ul.b {
  list-style-type: square;}
ol.c {
  list-style-type: upper-roman;}
ol.d {
  list-style-type: lower-alpha;}
```

**ul** (= unordered list): none | disc (= standaard-waarde) | circle | square;\
\*\*ol \*\*(= ordered list): decimal (1 2 3) | decimal-leading-zero (01 02 03) | lower-alpha (a b c) | upper-alpha (A B C) | lower-roman (i. ii. iii.) | upper-roman (I II III)

{% embed url="https://flems.io/#0=N4IgzgpgNhDGAuEAmIBcIB0ALeBbKIANCAGYCWMYaA2qAHYCGuEamO+RIsA9nYn6wA8AQgAiAeQDCAFQCaABQCiAAnZQAfAB06gtVp1YIDJPsFh4ATxj6ArlAwNlwbcuVQy5gLTmrET5YAHCFRlWDIAJ1gYAG5tAF9tbTsMACMnFzcPeG9LGH8LIJCwAEcbBnCIWLoEum1ue1h0uld3Lx88wODlGwCg8M9w7lwGOiqauvskJpasnN98wrduAHcIfoYoAKwGMe1BAHp2iFN9w2NTFO4kC309rAAmdWlDTLbcv07leUG+ywOH246ALqRQADyYARgym4JG6dG44SQa2Qr3gYFQB2BezsoSgDDAYAAvJoQAwSfpXIJ3OpJDCSBAIAdqRkqWQnkYmWyWdTabBHLS8ZyTnZAYIcVF8USSSlydy2bSSPTGftmc1lKz2QwhXKadw+coBVqVVydPsRYkgSDwbhIRBobCEUiKlNWmiMfssTp6rjJcSuLK1RqFUrtYHqdIOcaKeqeXr+fUjaqDvVRd6JQS-UgA5TY4qGaGc2yI4mTYXdfrDaHkxoLQdLtcTnoLdpOJAYAgyLwqOgAKw91AABhAcUI9CYLHQGAAVlRiDw+BABOhh6OQIxmKwMLACZx5-x4KxhwBdOJAA" %}

## list-style-image

```css
ul {
    list-style-image: url("../images/star.png");}
li {
    margin: 10px 0px 0px 0px;}
```

`list-style-image`: none (= standaardwaarde) | url;

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_list-style-image](https://www.w3schools.com/css/tryit.asp?filename=trycss_list-style-image)

## list-style-position

```css
ul {
    width: 150px;}
li {
    margin: 10px;}
ul.illuminations {
    list-style-position: outside;}
ul.season {
    list-style-position: inside;}
```

`list-style-position`: outside (= standaard-waarde) | inside;

**outside**: De markering bevindt zich links van de blok tekst. Indien de `list-style-position` niet uitdrukkelijk vermeld wordt, is dit de standaard weergave.\
**inside**: De marker zit vervat binnenin het tekstkader zelf.

try it yourself: [https://www.w3schools.com/css/tryit.asp?filename=trycss\_list-style-position](https://www.w3schools.com/css/tryit.asp?filename=trycss_list-style-position)

## list-style

```css
ul {
    list-style: inside circle;
    width: 300px;}
li {
    margin: 10px 0px 0px 0px;}
```

Bij `list-style` kunne zowel `list-style-type`, `list-style-position` en `list-style-image` benoemd worden.
