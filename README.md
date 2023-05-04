# NKPP
> Kleene Closure Property Path Query Optimization Based on Node Clustered Index
## BeSEPPI - Test Query Set

| id | query                                                        | remark |
| ----- | ------------------------------------------------------------ | ---- |
| 219  | `<http://www.ppbenchmark.com/e+2>*`                                         | $CIRCLE$ |
| 218  | `<http://www.ppbenchmark.com/e+>*`                              | $CIRCLE$ |
| 217  | `<http://www.ppbenchmark.com/e+3>*`                      | $PATH$ |
| 216  | `<http://www.ppbenchmark.com/e+1>*`               | $PATH$ |
| 215  | `<http://www.ppbenchmark.com/notExisting>*`    | $NOTEXIST$ |
| 214  | `<http://www.ppbenchmark.com/eSelf>*`     | $CIRCLE$ |
| 213  | `<http://www.ppbenchmark.com/e6>*`       | $PATH\quad LENGTH\quad  IS\quad 1$ |

## UOBM - Query Set

| id | query                                                        | type |
| ----- | ------------------------------------------------------------ | ---- |
| Q1  | `<http://semantics.crl.ibm.com/univ-bench-dl.owl#subOrganizationOf>*`                                         | $S − KPPQ$ |
| Q2  | `<http://semantics.crl.ibm.com/univ-bench-dl.owl#hasSameHomeTownWith>*`                              | $S − KPPQ$ |
| Q3  | `<http://semantics.crl.ibm.com/univ-bench-dl.owl#isFriendOf>*/name`                            | $S − KPPQ$ |
| Q4  | `(<http://semantics.crl.ibm.com/univ-bench-dl.owl#like>/<http://semantics.crl.ibm.com/univ-bench-dl.owl#telephone>)*`                      | $E − KPPQ$ |
| Q5  | `(<http://semantics.crl.ibm.com/univ-bench-dl.owl#love>/<http://semantics.crl.ibm.com/univ-bench-dl.owl#isMemberOf>/<http://semantics.crl.ibm.com/univ-bench-dl.owl#like>)*`               | $E − KPPQ$ |
| Q6  | `<http://semantics.crl.ibm.com/univ-bench-dl.owl#lastName>/(<http://semantics.crl.ibm.com/univ-bench-dl.owl#like>/<http://semantics.crl.ibm.com/univ-bench-dl.owl#telephone>)*`    | $C − KPPQ$ |
| Q7  | `<http://semantics.crl.ibm.com/univ-bench-dl.owl#like>*/<http://semantics.crl.ibm.com/univ-bench-dl.owl#subOrganizationOf>*`     | $C − KPPQ$ |
| Q8  | `<http://semantics.crl.ibm.com/univ-bench-dl.owl#like>*/<http://semantics.crl.ibm.com/univ-bench-dl.owl#subOrganizationOf>`       | $C − KPPQ$ |
| Q9  | `<http://semantics.crl.ibm.com/univ-bench-dl.owl#isFriendOf>/<http://semantics.crl.ibm.com/univ-bench-dl.owl#like>/<http://semantics.crl.ibm.com/univ-bench-dl.owl#subOrganizationOf>*`                  | $C − KPPQ$ |

## DBpedia - Query Set

| id | query                                                        | type |
| ----- | ------------------------------------------------------------ | ---- |
| Q1  | `<http://dbpedia.org/property/date>*`                                         | $S − KPPQ$ |
| Q2  | `<http://dbpedia.org/property/supporters>*`                              | $S − KPPQ$ |
| Q3  | `<http://dbpedia.org/property/allies>*`                            | $S − KPPQ$ |
| Q4  | `<http://dbpedia.org/property/power/massMain>*`                      | $S − KPPQ$ |
| Q5  | `<http://dbpedia.org/property/dialects>*`               | $S − KPPQ$ |
| Q6  | `<http://dbpedia.org/property/origin>*`    | $S − KPPQ$ |
| Q7  | `<http://dbpedia.org/property/team(s)_>*`     | $S − KPPQ$ |
| Q8  | `(<http://dbpedia.org/property/birthPlace>/<http://dbpedia.org/property/knownFor>)*`       | $E − KPPQ$ |
| Q9  | `(<http://dbpedia.org/property/knownFor>/<http://dbpedia.org/property/birthPlace>/<http://dbpedia.org/ontology/isPartOf>)*`                  | $E − KPPQ$ |
| Q10  | `<http://dbpedia.org/property/knownFor>*/<http://dbpedia.org/property/birthPlace>`                  | $C − KPPQ$ |
| Q11  | `<http://dbpedia.org/property/knownFor>/<http://dbpedia.org/property/birthPlace>/<http://dbpedia.org/ontology/location>*`                  | $C − KPPQ$ |
| Q12  | `<http://dbpedia.org/property/knownFor>*/<http://dbpedia.org/property/birthPlace>*`                  | $C − KPPQ$ |
