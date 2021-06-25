# **Análises**

## **Performance** :chart_with_downwards_trend:

O `Selection Sort` possui uma complexidade de `O(n^2)`, semelhante ao do  `Bubble Sort`, ou seja, sua performance em listas grandes deixa a desejar, além de ser
, em geral, inferior ao  `Insertion Sort`. Suas vantagens são a simplicidade e a performance sobre outros métodos em casos específicos, especialmente quando a 
memória auxiliar é um fator limitante.

Em termos de eficiência de tempo, o `Selection Sort` é quadrático, então existem outros métodos melhores que esse para aumentar a eficiência no tempo. Apesar disso,
uma das maiores vantagens do `Selection Sort` é que em seu pior caso, o número de trocas ainda é `n - 1`.

Dessa forma, o `Bubble Sort` não é o algoritmo mais viável de ser utilizado. Isso não significa que ele não possui vantagens, pois em uma lista ordenada, sua complexidade se torna
`O(n)`, enquanto outros algoritmos ainda possuem uma complexidade maior para esses casos de lista ordenada. Ainda assim, o `Insertion Sort` compartilha dessa vantagem.

Logo, é possível argumentar que a maior vantagem do `Bubble Sort` é sua baixa complexidade e fácil implementação.

| Performance em | Pior caso  |  Caso padrão  | Melhor caso |
| ------------------- | ------------------- | ------------------- | ------------------- |
|  Comparações |  O(n^2) | O(n) |  O(n) | 
|  Trocas |  O(n^2) |  O(n^2) |  O(1) |  


***

## **Implementação** :computer:
```
int n = arr.length;

        for (int i = 0; i < n-1; i++)
            for (int j = 0; j < n-i-1; j++)
            
if (arr[j] > arr[j+1])
                {
           	       int temp = arr[j];
                    arr[j] = arr[j+1];
                    arr[j+1] = temp;
                }
    }
```

### **Exemplificando**

- Considere o array [5,1,2,4,8]
- Veja que 5 é maior do que 1 (if arr[j]>arr[j+1]), logo, esses dois valores tem sua posição trocada, e o array passa a ser [1,5,2,4,8]. O valor 5 irá verificar o restante do array em sua passagem.
- Após terminar essa passagem, terá: [1,2,4,5,8]. 
- Ele repetirá o processo com o número 1,2,4,8, verificando cada posição, e então, faz uma última passagem para verificar tudo.

<img src="https://upload.wikimedia.org/wikipedia/commons/3/37/Bubble_sort_animation.gif" width=35% height=100%>

