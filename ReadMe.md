
# $computerman's dRep Platform

## Vote Context

| title                 | vote      | context                                                                          | transaction                                                                                                                   |
| -----                 | ----      | -------                                                                          | -----------                                                                                                                   |
| Name Chang 2 'Hosky'  | yes       | [1.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/1.jsonld)               | [cardanoscan](https://cardanoscan.io/vote/a3e6d4ef0570bf6db0e4d926b1583b920fae55e16f467adb4faba4da9530238f)  |
| Ikigai                | yes       | [2_Ikigai.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/2_Ikigai.jsonld)        | [cardanoscan](https://cardanoscan.io/vote/897b19c9c0d28adc75d560ac874f819c0c8b4bd050961b7b2c9f973ecf6b488b)  |
| Increase K            | abstain   | [3_increaseK.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/3_increaseK.jsonld)     | [cardanoscan](https://cardanoscan.io/vote/8b9903e6a22933b6d987f1016e9613da85693e314df8ea8d28f3f761b75a407f)  |
| Name Chang 2 'Plomin' | yes       | [4_plomin.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/4_plomin.jsonld)     | [cardanoscan](https://cardanoscan.io/vote/e8fa84db4ee42927c33a3aa3bec2bd4680aa1ffdd1da526151d50a24a53d4b0d)  |
| Cardano Constitution to Replace the Interim Constitution | yes | [5_constitution.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/5_constitution.jsonld) | [cardanoscan](https://cardanoscan.io/vote/c6c6a876dbb701c7d955def074b3f4987fa1893d6803b568c8da16582c2bf6bf) |
|Decrease Treasury Tax from 20% to 10%                  | No      | [6_tax_decrease.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/6_tax_decrease.jsonld) | [cardanoscan](https://cardanoscan.io/vote/f5b449599ed527e010f8fc2815c1607ae00d5eac683735b2c355b0012f4bef92)    |
| 2025 Roadmap (first tentative vote)   | No | [7a_roadmap.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/7a_roadmap.jsonld) | [cardanoscan](https://cardanoscan.io/vote/43b5f6911416f535f38a1b78800e2b35ce3676449ee3b990e6e584c717779631)
| 2025 & 2026 Minimum NCL | Yes | [8_ncl.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/8_ncl.jsonld) | [cardanoscan](https://cardanoscan.io/vote/2e8b7b3bec08faf5d2cacba70372c7919ff1083127da9b7bd77b6d8df5847183)
| 2025 NCL | Yes | [9_ncl.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/9_ncl.jsonld) | [cardanoscan](https://cardanoscan.io/vote/2c5a12f4b61e9b24891a3d3bcaecb31ce13e82da05c94a9e28e3cc959512d643) |
| 2025 Cardano NCL | Yes | [10_ncl.jsonld](https://github.com/willpiam/drep/blob/master/vote_context/10_ncl.jsonld) | [cardanoscan](https://cardanoscan.io/vote/723ffd516e67b18ea4795119f670f30872b757240687776dbcab6ba6091f2019) |

## Vote Context (Markdown)

- [6_tax_decrease](https://github.com/willpiam/drep/blob/master/vote_context/markdown/6_tax_decrease.md)
- [7a_roadmap](https://github.com/willpiam/drep/blob/master/vote_context/markdown/7a_roadmap.md)
- [8_ncl_2025_and_2026](https://github.com/willpiam/drep/blob/master/vote_context/markdown/8_ncl_2025_and_2026.md)
- [9_ncl_2025](https://github.com/willpiam/drep/blob/master/vote_context/markdown/9_ncl_2025.md)
- [10_ncl_2025_b](https://github.com/willpiam/drep/blob/master/vote_context/markdown/10_ncl_2025_b.md)

## How I hash 

These two methods should yield the same hash.

### Method 1: Web Portal

1. Navigate to https://toolkitbay.com/tkb/tool/BLAKE2b_256
2. select `File input`
3. Upload file
4. press `Process from file`


### Method 2: CLI

    b2sum -l 256 <path_to_file>

## Commitment Transactions

| Tx Link | Document Hash |
| ------- | ------------- |
| [Voltaire Paper Draft 1](https://adastat.net/transactions/beca42f91b669045bfc44c9f949dce8e11d7665aafa8c1aa5b5c4eeb6914df3e) | 254999bc30cef78f78e52c233fcdb12c4a3967ac1f99c27863f513f728f61d1d |