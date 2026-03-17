A empresa de telecomunicações Poxim Tech está construindo um sistema de comunicação baseado na priorização de pacotes em redes TCP/IP para implementação de qualidade de serviço (QoS).

Os dados de cada pacote são sequências de bytes de tamanho variável, limitados a 512 bytes. Os níveis de prioridade variam entre 0 (mínimo) e 63 (máximo), considerando que o roteador possui um limite máximo de bytes que consegue processar por vez.

Sempre que a capacidade de processamento do roteador for atingida ou não for possível receber mais nenhum pacote, é feita a ordenação dos pacotes levando em consideração os seus respectivos níveis de priorização.

## Formato de arquivo de entrada

```text
[Número de pacotes (n)] [Quantidade de bytes]
[Prioridade do pacote1] [#m1 Tamanho do pacote] [B1] ... [Bm1]
.
.
.
[Prioridade do pacoten] [#mn Tamanho do pacote] [B1] ... [Bmn]
```

## Exemplo de entrada

```text
6 8
0 3 01 02 03
2 4 06 07 08 09
63 2 0F 10
15 6 11 12 13 14 15 16
32 5 0A 0B 0C 0D 0E
11 2 04 05
```

## Formato de arquivo de saída

Quando uma quantidade máxima de dados é recebida, é feita a ordenação dos pacotes armazenados para priorização do roteamento.

## Exemplo de saída

```text
|06,07,08,09|01,02,03|
|0F,10|11,12,13,14,15,16|
|0A,0B,0C,0D,0E|04,05|
```

---
