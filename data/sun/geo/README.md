# Mapping the Johns Hopkins Geolocations to standards

Unfortunately, the Johns Hopkins dataset uses non standard country names such as `Korea, Soouth`. For our mapping efforts, we created a cross reference list that attempts to map these contries onto their original name.

```
"name","ADM0_A3","ISO_3_code_i"
"Aruba","ABW",533
"Afghanistan","AFG",4
"Islamic Republic of Afghanistan","AFG",4
...
"Congo, The Democratic Republic of the","COD",180
"Congo","COG",178
"Republic of the Congo","COG",178
...
"Congo (Brazzaville)","COD",180
```

Data sources to consolidate these data used are
* pycountry package
* [ISO free download page](https://www.iso.org/iso-3166-country-codes.html)
* [Wikipedia](https://en.wikipedia.org/wiki/ISO_3166-1_alpha-3#Officially_assigned_code_elements)
* [IBAN country codes](https://www.iban.com/country-codes)
* [UN population metadata](https://population.un.org/wpp/Download/Files/4_Metadata/WPP2019_F01_LOCATIONS.XLSX)
* manual review and assignment

| Field   | Semantics                                  | Type |
|---------|--------------------------------------------|------|
| name    | country name used in Johns Hopkins dataset | string |
| ADM0_A3 | ISO country code | string |
| ISO_3_code_i | ISO 3166/UN country code | int |
