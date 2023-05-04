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

| index | query                                                        | type |
| ----- | ------------------------------------------------------------ | ---- |
| L_Q1  | $subOrganizationOf^{\*}$                                          | $KS_{one}$ |
| L_Q2  | $worksFor/subOrganizationOf^{\*}$                               | $KS_{one}$ |
| L_Q3  | $headOf/subOrganizationOf^{\*}/name$                            | $KS_{one}$ |
| L_Q4  | $(headOf/subOrganizationOf/memberOf)^{\*}$                      | $KS_{fm}$ |
| L_Q5  | $ResearchGroup/subOrganizationOf^{\*}/University$               | $KS_{one}$ |
| L_Q6  | $FullProfessor/headOf/subOrganizationOf^{\*}/typeUniversity$    | $KS_{one}$ |
| L_Q7  | $ResearchGroup/subOrganizationOf^{\*}/University/ResGroup^{\*}$     | $KS_{one}$ |
| L_Q8  | $(worksFor/subOrganizationOf^{\*})^{\*}$                           | $KS_{co}$ |
| L_Q9  | $((headOf/subOrganizationOf)^{\*}/memberOf)^{\*}$                  | $KS_{co}$ |
| L_Q10 | $(FullProfessor/headOf)^{\*}/(subOrganizationOf^{\*}/typeUniversity)^{\*}$ | $KS_{co}$ |
