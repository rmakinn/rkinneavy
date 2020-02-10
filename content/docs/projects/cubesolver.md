---
Title: "Cubesolver"
Tags:
- projects
- cubing
---

# A Solution Assistant for CFOP

Inspiration: 

- https://bitbucket.org/ericvogler/cubepractice01/src/master/
    - https://pastebin.com/UzvQJFdU


Related posts:

- https://www.speedsolving.com/threads/cfop-efficiency-and-multi-slotting.45301/post-930395

Links:

http://zunny.com/RUBIK.HTM

---

## AlgDB API

set up initial options request
then post
then a get with content as:

`
Host: cubiclealgdbserver.azurewebsites.net
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:68.0) Gecko/20100101 Firefox/68.0
Accept: application/json, text/plain, */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate
Origin: http://algdb.net
Connection: keep-alive
Referer: http://algdb.net/puzzle/333/zbll-zbllas
`

reponse returns a JSON object as:

```json

{"JSON":[{"id":"640438b4-4f72-4605-87b4-6df13d9b6f0e","name":"ZBLL AS 1","shortName":"zbllas1","caseGroupName":"ZBLL AS","caseGroupNameWithParents":"ZBLL-ZBLL AS","caseGroupShortName":"zbllas","puzzleName":"3x3","puzzleShortName":"333","caseAlgs":[{"moves":"y' R U R' B' U R U' R' U' B U2 R U2 R'"},{"moves":"R U2 R' U R U R' U2 y' R' U' R U R' U R U R' U' R"},{"moves":"y' R U R' U' L' U2 R U' R' U2 L U' R U2 R'"}],"imageType":"puzzleImageGenerator","pigPuzzle":"3","pigCase":"y' R U R' U' L' U2 R U' R' U2 L U' R U2 R'","pigStage":"zbll","pigView":"plan","caseTypeEnum":"permutation"}, 

...

```
