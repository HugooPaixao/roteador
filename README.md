# Quick Sort

A empresa de desenvolvimento de sistemas Poxim Tech está realizando um experimento para determinar qual variante do algoritmo de ordenação crescente do Quicksort apresenta o melhor resultado para um determinado conjunto de sequências numéricas.

Neste experimento foram utilizadas as seguintes variantes:

* Lomuto padrão (LP)
* Lomuto por mediana de 3 (LM)
* Lomuto por pivô aleatório (LA)
* Hoare padrão (HP)
* Hoare por mediana de 3 (HM)
* Hoare por pivô aleatório (HA)

## Técnicas de escolha do pivô

* Mediana de 3: V1 = V[n/4], V2 = V[n/2], V3 = V[3n/4]
* Aleatório: Va = V[ini + |V[ini]| mod n]

## Formato de arquivo de entrada

```text
[#n total de vetores]
[#N1 números do vetor 1]
[E1] ... [EN1]
...
[#Nn números do vetor n]
[E1] ... [ENn]
```

## Exemplo de entrada

```text
4
6
-23 10 7 -34 432 3
4
955 -32 1 9
7
834 27 39 19 3 -1 -33
10
847 38 -183 -13 94 -2 -42 54 28 100
```

## Formato de arquivo de saída

Para cada vetor é impressa a quantidade total de números N e a sequência com ordenação estável contendo o número de trocas e de chamadas.

## Exemplo de saída

```text
[6]:LP(15),HP(16),LM(19),HM(19),HA(20),LA(22)
[4]:LP(10),HP(10),LM(11),LA(11),HM(12),HA(12)
[7]:HP(17),LM(18),LP(23),HM(26),HA(27),LA(30)
[10]:LM(28),HP(28),LP(33),HA(35),HM(37),LA(38)
```

---

> Todas as entradas e saídas seguem rigorosamente os formatos das descrições.
> O algoritmo foi implementado para fins acadêmicos.