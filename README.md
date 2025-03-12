Andrew Kallmeyer, Gabriel Geyer, Evan Taylor

## Case k = 2:
- **xS**: 400323194
- **Hash value**: 00f99f47c24ca614de5029215292b3bad2e2068f1ddfc450d6d4d576f7dcdc7a
- **Time elapsed**: 3s
- **Trials**: 100

## Case k = 3:
- **xS**: 1855000508
- **Hash value**: 00018dd9343abce11160d7cfbeb1bdedaa3fbcc2b4070d5056c415e88ba7a978
- **Time elapsed**: 3s
- **Trials**: 10000

## Case k = 4:
- **xS**: 1308524504
- **Hash value**: 00009cf104cef4b49bfc3c46a1ede730fd238e4cae198d6c671cf879dd5d9a8e
- **Time elapsed**: 3s
- **Trials**: 100000

## Case k = 5:
- **xS**: 741231304
- **Hash value**: 000001641efedb4e13e1535f08da1c642b9325a755485f36581b86ecd6038d09
- **Time elapsed**: 5s
- **Trials**: 1000000

## Case k = 6:
- **xS**: 1144692896
- **Hash value**: 000000719406419f557703a35cb85d7664ef29b4e11af90e4d571ace22ee9a06
- **Time elapsed**: 66s
- **Trials**: 100000000

## Case k = 7 (GCP trial):
- **xS**: 1875148904
- **Hash value**: 0000000a875f94d5d2e4606243dceaeb2e61e761da0f2eba2a6d042750c3c8eb
- **Time elapsed**: 2966s (49.4m)
- **Trials**: 1000000000

---

This approach varies from the randomized approach only in the way the nonces are allocated (i.e., the line changed in the `main.scala` file). It confirms that all possible nonce assignments in the trial range are covered, as opposed to the randomized approach, which stops when it gets a hit. This does not speed up the process, and only ensures that all nonces are checked. On average, it could be concluded that this approach is actually slower with larger difficulties.
