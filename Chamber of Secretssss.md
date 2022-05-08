# Chamber of Secretsss Writeup
## DDC 2022
###### Skrevet af ketamin 07-05-2022
---
##### Description
Sværhedsgrad: **Medium**

Hemmelighedernessss kammer er åbnet igen, men hvisss du vil ind, ssssskal du forbi mig førssssst!
```term
nc chamber-of-secretssss.hkn 55555
```

##### Writeup
Det første vi bliver mødt med, er to valgmuligheder
```term
What would you like to do?

1: Get a ssssneak peek

2: Accessss my chamber

```
Valgmulighed 2 giver et input felt og spørger om en kode. Valgmulighed 1 giver følgende output:
```
Thissss issss how I check if you are worthy of accessssing my ssssecret chamber.
Good luck underssstanding it, it'sssss in parsssseltongue:

  8           0 LOAD_FAST                0 (codeword)
              2 LOAD_METHOD              0 (startswith)
              4 LOAD_CONST               1 ('DDC{')
              6 CALL_METHOD              1
              8 POP_JUMP_IF_FALSE       10 (to 20)
             10 LOAD_FAST                0 (codeword)
             12 LOAD_METHOD              1 (endswith)
             14 LOAD_CONST               2 ('}')
             16 CALL_METHOD              1
             18 POP_JUMP_IF_TRUE        12 (to 24)
        >>   20 LOAD_ASSERTION_ERROR
             22 RAISE_VARARGS            1

  9     >>   24 LOAD_GLOBAL              2 (len)
             26 LOAD_FAST                0 (codeword)
             28 CALL_FUNCTION            1
             30 LOAD_CONST               3 (39)
             32 COMPARE_OP               2 (==)
             34 POP_JUMP_IF_TRUE        20 (to 40)
             36 LOAD_ASSERTION_ERROR
             38 RAISE_VARARGS            1

 10     >>   40 LOAD_FAST                0 (codeword)
             42 LOAD_CONST               4 (21)
             44 BINARY_SUBSCR
             46 LOAD_CONST               5 ('d')
             48 COMPARE_OP               2 (==)
             50 POP_JUMP_IF_TRUE        28 (to 56)
             52 LOAD_ASSERTION_ERROR
             54 RAISE_VARARGS            1

 11     >>   56 LOAD_FAST                0 (codeword)
             58 LOAD_CONST               6 (13)
             60 BINARY_SUBSCR
             62 LOAD_GLOBAL              3 (chr)
             64 LOAD_GLOBAL              4 (ord)
             66 LOAD_FAST                0 (codeword)
             68 LOAD_CONST               7 (0)
             70 BINARY_SUBSCR
             72 CALL_FUNCTION            1
             74 LOAD_GLOBAL              4 (ord)
             76 LOAD_FAST                0 (codeword)
             78 LOAD_CONST               8 (9)
             80 BINARY_SUBSCR
             82 CALL_FUNCTION            1
             84 BINARY_XOR
             86 CALL_FUNCTION            1
             88 COMPARE_OP               2 (==)
             90 POP_JUMP_IF_TRUE        48 (to 96)
             92 LOAD_ASSERTION_ERROR
             94 RAISE_VARARGS            1

 12     >>   96 LOAD_FAST                0 (codeword)
             98 LOAD_METHOD              5 (index)
            100 LOAD_CONST               9 ('my')
            102 CALL_METHOD              1
            104 LOAD_CONST              10 (23)
            106 COMPARE_OP               2 (==)
            108 POP_JUMP_IF_TRUE        57 (to 114)
            110 LOAD_ASSERTION_ERROR
            112 RAISE_VARARGS            1

 13     >>  114 LOAD_FAST                0 (codeword)
            116 LOAD_CONST              11 (8)
            118 LOAD_CONST              12 (12)
            120 BUILD_SLICE              2
            122 BINARY_SUBSCR
            124 LOAD_GLOBAL              6 (b64decode)
            126 LOAD_CONST              13 ('aDR2Mw==')
            128 CALL_FUNCTION            1
            130 LOAD_METHOD              7 (decode)
            132 CALL_METHOD              0
            134 COMPARE_OP               2 (==)
            136 POP_JUMP_IF_TRUE        71 (to 142)
            138 LOAD_ASSERTION_ERROR
            140 RAISE_VARARGS            1

 14     >>  142 LOAD_FAST                0 (codeword)
            144 LOAD_CONST              14 (6)
            146 LOAD_CONST              15 (3)
            148 LOAD_CONST              16 (-1)
            150 BUILD_SLICE              3
            152 BINARY_SUBSCR
            154 LOAD_CONST              17 ('u0y')
            156 COMPARE_OP               2 (==)
            158 POP_JUMP_IF_TRUE        82 (to 164)
            160 LOAD_ASSERTION_ERROR
            162 RAISE_VARARGS            1

 15     >>  164 LOAD_FAST                0 (codeword)
            166 LOAD_CONST              18 (37)
            168 BINARY_SUBSCR
            170 LOAD_FAST                0 (codeword)
            172 LOAD_CONST              19 (26)
            174 BINARY_SUBSCR
            176 COMPARE_OP               2 (==)
            178 POP_JUMP_IF_TRUE        92 (to 184)
            180 LOAD_ASSERTION_ERROR
            182 RAISE_VARARGS            1

 16     >>  184 LOAD_FAST                0 (codeword)
            186 LOAD_CONST              20 (28)
            188 LOAD_CONST              18 (37)
            190 BUILD_SLICE              2
            192 BINARY_SUBSCR
            194 LOAD_CONST              21 ('sS5')
            196 LOAD_GLOBAL              8 (int)
            198 LOAD_FAST                0 (codeword)
            200 LOAD_CONST              22 (27)
            202 BINARY_SUBSCR
            204 CALL_FUNCTION            1
            206 BINARY_MULTIPLY
            208 COMPARE_OP               2 (==)
            210 POP_JUMP_IF_TRUE       108 (to 216)
            212 LOAD_ASSERTION_ERROR
            214 RAISE_VARARGS            1

 17     >>  216 LOAD_GLOBAL              4 (ord)
            218 LOAD_FAST                0 (codeword)
            220 LOAD_CONST              19 (26)
            222 BINARY_SUBSCR
            224 CALL_FUNCTION            1
            226 LOAD_CONST              23 (115)
            228 COMPARE_OP               4 (>)
            230 POP_JUMP_IF_FALSE      124 (to 248)
            232 LOAD_GLOBAL              4 (ord)
            234 LOAD_FAST                0 (codeword)
            236 LOAD_CONST              19 (26)
            238 BINARY_SUBSCR
            240 CALL_FUNCTION            1
            242 LOAD_CONST              24 (117)
            244 COMPARE_OP               0 (<)
            246 POP_JUMP_IF_TRUE       126 (to 252)
        >>  248 LOAD_ASSERTION_ERROR
            250 RAISE_VARARGS            1

 18     >>  252 LOAD_GLOBAL              8 (int)
            254 LOAD_FAST                0 (codeword)
            256 LOAD_CONST              22 (27)
            258 BINARY_SUBSCR
            260 CALL_FUNCTION            1
            262 LOAD_CONST              10 (23)
            264 LOAD_GLOBAL              8 (int)
            266 LOAD_FAST                0 (codeword)
            268 LOAD_CONST              25 (16)
            270 BINARY_SUBSCR
            272 CALL_FUNCTION            1
            274 BINARY_MODULO
            276 COMPARE_OP               2 (==)
            278 POP_JUMP_IF_TRUE       142 (to 284)
            280 LOAD_ASSERTION_ERROR
            282 RAISE_VARARGS            1

 19     >>  284 LOAD_FAST                0 (codeword)
            286 LOAD_CONST              26 (14)
            288 LOAD_CONST               4 (21)
            290 BUILD_SLICE              2
            292 BINARY_SUBSCR
            294 LOAD_CONST              27 ('s')
            296 LOAD_METHOD              9 (join)
            298 LOAD_CONST              28 ('a5S3')
            300 CALL_METHOD              1
            302 COMPARE_OP               2 (==)
            304 POP_JUMP_IF_TRUE       155 (to 310)
            306 LOAD_ASSERTION_ERROR
            308 RAISE_VARARGS            1

 20     >>  310 LOAD_FAST                0 (codeword)
            312 LOAD_METHOD             10 (count)
            314 LOAD_CONST              29 ('_')
            316 CALL_METHOD              1
            318 LOAD_CONST              30 (4)
            320 COMPARE_OP               2 (==)
            322 POP_JUMP_IF_TRUE       164 (to 328)
            324 LOAD_ASSERTION_ERROR
            326 RAISE_VARARGS            1
        >>  328 LOAD_CONST               0 (None)
            330 RETURN_VALUE
```
Dette må være den måde serveren tjekker om adgangskoden er korrekt. Dette ligner [Python Dissasembly](https://docs.python.org/3/library/dis.html). En analyse af hvert enkelt tjek ville kunne fortælle os hvad koden er.

**Første tjek**
```term
 8            0 LOAD_FAST                0 (codeword)
              2 LOAD_METHOD              0 (startswith)
              4 LOAD_CONST               1 ('DDC{')
              6 CALL_METHOD              1
              8 POP_JUMP_IF_FALSE       10 (to 20)
             10 LOAD_FAST                0 (codeword)
             12 LOAD_METHOD              1 (endswith)
             14 LOAD_CONST               2 ('}')
             16 CALL_METHOD              1
             18 POP_JUMP_IF_TRUE        12 (to 24)
        >>   20 LOAD_ASSERTION_ERROR
             22 RAISE_VARARGS            1
```

Det antages at vores input bliver gemt i variablen codeword. Der bliver tjekket om codeword starter med stringet 'DDC{' og slutter med '}'.
Vi ved nu følgende om kodeorder
```term
DDC{...?}
```

**Andet tjek**
```term
  9     >>   24 LOAD_GLOBAL              2 (len)
             26 LOAD_FAST                0 (codeword)
             28 CALL_FUNCTION            1
             30 LOAD_CONST               3 (39)
             32 COMPARE_OP               2 (==)
             34 POP_JUMP_IF_TRUE        20 (to 40)
             36 LOAD_ASSERTION_ERROR
             38 RAISE_VARARGS        
```
Der tjekkes om længden af codeword er 39
```term
DDC{----------------------------------}
```

**Tredje tjek**
```term
 10     >>   40 LOAD_FAST                0 (codeword)
             42 LOAD_CONST               4 (21)
             44 BINARY_SUBSCR
             46 LOAD_CONST               5 ('d')
             48 COMPARE_OP               2 (==)
             50 POP_JUMP_IF_TRUE        28 (to 56)
             52 LOAD_ASSERTION_ERROR
             54 RAISE_VARARGS
```
En undersøgelse af BINARY_SUBSCR viser at der tjekkes om index 21 af codeword er lig med 'd'
```term
DDC{-----------------d----------------}
```

**Femte tjek**
```term
 12     >>   96 LOAD_FAST                0 (codeword)
             98 LOAD_METHOD              5 (index)
            100 LOAD_CONST               9 ('my')
            102 CALL_METHOD              1
            104 LOAD_CONST              10 (23)
            106 COMPARE_OP               2 (==)
            108 POP_JUMP_IF_TRUE        57 (to 114)
            110 LOAD_ASSERTION_ERROR
            112 RAISE_VARARGS            1
```
Tjekker om 'my' stringets index er lig med 23
```term
DDC{-----------------d-my-------------}
```
**Sjette tjek**
```term
 13     >>  114 LOAD_FAST                0 (codeword)
            116 LOAD_CONST              11 (8)
            118 LOAD_CONST              12 (12)
            120 BUILD_SLICE              2
            122 BINARY_SUBSCR
            124 LOAD_GLOBAL              6 (b64decode)
            126 LOAD_CONST              13 ('aDR2Mw==')
            128 CALL_FUNCTION            1
            130 LOAD_METHOD              7 (decode)
            132 CALL_METHOD              0
            134 COMPARE_OP               2 (==)
            136 POP_JUMP_IF_TRUE        71 (to 142)
            138 LOAD_ASSERTION_ERROR
            140 RAISE_VARARGS            1
```
Udfører først et string slice af codeword (codeword[8:12]) og tjekker om et decoded base64 string (decoder til h4v3) er lig med dette slice.
```term
DDC{----h4v3---------d-my-------------}
```
**Syvende tjek**
```term
 14     >>  142 LOAD_FAST                0 (codeword)
            144 LOAD_CONST              14 (6)
            146 LOAD_CONST              15 (3)
            148 LOAD_CONST              16 (-1)
            150 BUILD_SLICE              3
            152 BINARY_SUBSCR
            154 LOAD_CONST              17 ('u0y')
            156 COMPARE_OP               2 (==)
            158 POP_JUMP_IF_TRUE        82 (to 164)
            160 LOAD_ASSERTION_ERROR
            162 RAISE_VARARGS            1
```
Laver et string slice af codeword (codeword[6:3:-1]) og tjekker om 'u0y'. Bemærk -1 i slice.
```term
DDC{y0u-h4v3---------d-my-------------}
```
**Ottende tjek**
```term
 15     >>  164 LOAD_FAST                0 (codeword)
            166 LOAD_CONST              18 (37)
            168 BINARY_SUBSCR
            170 LOAD_FAST                0 (codeword)
            172 LOAD_CONST              19 (26)
            174 BINARY_SUBSCR
            176 COMPARE_OP               2 (==)
            178 POP_JUMP_IF_TRUE        92 (to 184)
            180 LOAD_ASSERTION_ERROR
            182 RAISE_VARARGS            1
```
Tjekker om codewords index 37 og 26 er ens. 
```term
DDC{y0u-h4v3---------d-my-x----------x}
```
**Niende tjek**
```term
 16     >>  184 LOAD_FAST                0 (codeword)
            186 LOAD_CONST              20 (28)
            188 LOAD_CONST              18 (37)
            190 BUILD_SLICE              2
            192 BINARY_SUBSCR
            194 LOAD_CONST              21 ('sS5')
            196 LOAD_GLOBAL              8 (int)
            198 LOAD_FAST                0 (codeword)
            200 LOAD_CONST              22 (27)
            202 BINARY_SUBSCR
            204 CALL_FUNCTION            1
            206 BINARY_MULTIPLY
            208 COMPARE_OP               2 (==)
            210 POP_JUMP_IF_TRUE       108 (to 216)
            212 LOAD_ASSERTION_ERROR
            214 RAISE_VARARGS            1
```
Denher er lidt tricky. Efter lidt afprøvning findes det frem til at der tjekkes om 'sS5' optræder i stringslicet [28:37] ligeså mange gange som tallet der står på index 27. Eftersom stringslicet er 9 karakter langt, giver det mening at der skal stå 3 på index 27's pads og 'sS5sS5sS5' i slicet
```term
DDC{y0u-h4v3---------d-my-x-sS5sS5sS5x}
```
**Tiende tjek**
```term
 17     >>  216 LOAD_GLOBAL              4 (ord)
            218 LOAD_FAST                0 (codeword)
            220 LOAD_CONST              19 (26)
            222 BINARY_SUBSCR
            224 CALL_FUNCTION            1
            226 LOAD_CONST              23 (115)
            228 COMPARE_OP               4 (>)
            230 POP_JUMP_IF_FALSE      124 (to 248)
            232 LOAD_GLOBAL              4 (ord)
            234 LOAD_FAST                0 (codeword)
            236 LOAD_CONST              19 (26)
            238 BINARY_SUBSCR
            240 CALL_FUNCTION            1
            242 LOAD_CONST              24 (117)
            244 COMPARE_OP               0 (<)
            246 POP_JUMP_IF_TRUE       126 (to 252)
        >>  248 LOAD_ASSERTION_ERROR
            250 RAISE_VARARGS            1
```

Kører ord() på index 26 af og tjekker om den er imellem 115 og 117 dvs. 116 hvis du nu skulle være i tvivl. Dette svarer til 't'
```term
DDC{y0u-h4v3---------d-my-t3sS5sS5sS5t}
```

**Tolvte tjek**
```term
 19     >>  284 LOAD_FAST                0 (codeword)
            286 LOAD_CONST              26 (14)
            288 LOAD_CONST               4 (21)
            290 BUILD_SLICE              2
            292 BINARY_SUBSCR
            294 LOAD_CONST              27 ('s')
            296 LOAD_METHOD              9 (join)
            298 LOAD_CONST              28 ('a5S3')
            300 CALL_METHOD              1
            302 COMPARE_OP               2 (==)
            304 POP_JUMP_IF_TRUE       155 (to 310)
            306 LOAD_ASSERTION_ERROR
            308 RAISE_VARARGS            1
```
Sammenligner string slicet [14:21] og 's'.join('a5S3') hvilket svarer til as5sSs3
```term
DDC{y0u-h4v3--as5sSs3d-my-t3sS5sS5sS5t}
```

**Sidste tjek**
```term
 20     >>  310 LOAD_FAST                0 (codeword)
            312 LOAD_METHOD             10 (count)
            314 LOAD_CONST              29 ('_')
            316 CALL_METHOD              1
            318 LOAD_CONST              30 (4)
            320 COMPARE_OP               2 (==)
            322 POP_JUMP_IF_TRUE       164 (to 328)
            324 LOAD_ASSERTION_ERROR
            326 RAISE_VARARGS            1
        >>  328 LOAD_CONST               0 (None)
            330 RETURN_VALUE
```
Tæller om der er 4 "\_" i codeword. Herfra kan man godt regne ud at flaget er:
```term
DDC{y0u_h4v3_pas5sSs3d_my_t3sS5sS5sS5t}
```