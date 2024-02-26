# Daten Komprimieren ANNEX

## 1. Huffman-Algorithmus

Dateisysteme haben auch eine Baumstruktur.

Ein binärer Baum hat bei jedem Knoten, immer höchstens 2 Kinder, dies ist bei nicht binären Bäumen nicht so, da gibt es meistens keine Begrenzung von Kindern.

## 2. Huffman-Algorithmus

### Encode Huffman-Algorithmus

![Huffman Tree](Huffman-Tree.png)

```python
import heapq
from collections import defaultdict

def encode(frequency):
    heap = [[weight, [symbol, ""]] for symbol, weight in frequency.items()]
    heapq.heapify(heap)
    while len(heap) > 1:
        lo = heapq.heappop(heap)
        hi = heapq.heappop(heap)
        for pair in lo[1:]:
            pair[1] = '0' + pair[1]
        for pair in hi[1:]:
            pair[1] = '1' + pair[1]
        heapq.heappush(heap, [lo[0] + hi[0]] + lo[1:] + hi[1:])
    return sorted(heapq.heappop(heap)[1:], key=lambda p: (len(p[-1]), p))

word = "Twitchstreamer"
frequency = defaultdict(int)
for symbol in word:
    frequency[symbol] += 1

huff = encode(frequency)
print("Symbol".ljust(10) + "Huffman Code")
for p in huff:
    print(p[0].ljust(10) + p[1])

"""
Symbol    Huffman Code
t         00
e         100
r         110
T         0100
a         0101
c         0110
h         0111
i         1010
m         1011
s         1110
w         1111
"""

code_table = {p[0]: p[1] for p in huff}

huffman_code = "".join(code_table[char] for char in word)

print("Huffman Code for the word:", huffman_code)
# 110101101000101110001100111111101001101100000010
```

### Decode Huffman-Algorithmus

```python
huffman_code = "110101101000101110001100111111101001101100000010"
code_table = {
    "00": "e",
    "011": "a",
    "010": "s",
    "101": "n",
    "1101": "N",
    "1100": "b",
    "1111": "r",
    "1110": "j",
    "1001": "u",
    "1000": "g"
}

decoded_word = ""
while huffman_code:
    for code, char in code_table.items():
        if huffman_code.startswith(code):
            decoded_word += char
            huffman_code = huffman_code[len(code):]
            break

print(decoded_word) # Nasenbaerjunges
```

## 3. RLC

1 Blau
