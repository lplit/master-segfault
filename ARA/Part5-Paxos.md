# Cours

// A completer

# TD

## Q1

> Rappelez les proprietes de la diffusion fiable et du consensus

Diffusion fiable:
-
- Accord
    - Si un processus correct delivre, tout les corrects doivent delivrer
- Validite
    - Si un processus correct `p`, `R_Broadcast(m)`, alors `p` fait `R_deliver(m)`
- Integrite uniforme
    - Pour tout `m`, chaque processus `p` fait au plus 1 fois `r_deliver(m)`, `m` diffuse par 1 `r_broadcast(m)`
    - ^ Chaque message est delivre exactemment une fois

Consensus:
-

- Accord:
    - 2 procssus corrects ne peuvent decider differemment
- Validite:
    - Decision sur 1 valeur propose
- Integrite:
    - Tout processus decide au plus 1 fois
- Terminaison
    - Tout correct decide

## Q2

> Proposez un algo simple de diffusion fiable

Des qu'on recois un message, on retransmet.

> \>\>fig1 ARA/td4:consnesus here<<

```
R_broadcast(m):
    send m to all

upon reception of m:
    if m received first time:
        if sender(m) != p:
            send m to all
            r_deliver(m)
```

## Q3

> Executez l'algorithme sans faute en considerant 3 processus

> \>\>fig2 ARA/td4:consnesus here<<

## Q4

> Executez l'algo en considerant 3 processus avec le processus 2 qui tombe en pasnne

> \>\>fig3 ARA/td4:consnesus here<<

## Q5

> Quel est l'impact d'une fausse suspicion? Est-il possible que deux coordinateurs differents diffusent une decision? Illustrez votre reponse par un scenario.

Fausse suspicion du coordinateur:
 
- Cas1: Coordinateur suspecte par 1 majorite
- > \>\>fig4 ARA/td4:consnesus here<<