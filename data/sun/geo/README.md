# Mapping the Johns Hopkins Geolocations to standards

Unfortunately, the Johns Hopkins dataset uses non standard country names such as `Korea, Soouth`. For our mapping efforts, we created a cross reference list that attempts to map these contries onto their original name.

```
"Country/Region","ADMIN","ADM0_A3","MANUAL"
"Afghanistan","Afghanistan","AFG",0
"Albania","Albania","ALB",0
"Algeria","Algeria","DZA",0
"Andorra","","",-1
...
"Congo (Brazzaville)","Democratic Republic of the Congo","COD",0
"Congo (Kinshasa)","Republic of the Congo","COG",1
...
```

| Field   | Semantics                                  | Type |
|---------|--------------------------------------------|------|
| Country | country name used in Johns Hopkins dataset | string | string |
| ADMIN   | country name used by http://www.naturalearthdata.com/ | string |
| ADM0_A3 | ISO country code | string |
| MANUAL | Flag indicating resolution method: 0=automatic, -1=cannot be mapped, 1=manual mapping | enum |
