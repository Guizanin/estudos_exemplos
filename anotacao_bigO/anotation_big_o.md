# ⏳ Notação Big O

A **notação Big O** descreve a complexidade do tempo ou espaço de um algoritmo.

## 📝 Tabela de Complexidade

| **Notação**  | **Nome**          | **Exemplo**                  |
| ------------ | ----------------- | ---------------------------- |
| **O(1)**     | Tempo constante   | Acessar elemento em um array |
| **O(log n)** | Tempo logarítmico | Busca binária                |
| **O(n)**     | Tempo linear      | Percorrer um array           |
| **O(n²)**    | Tempo quadrático  | Ordenação por seleção        |
| **O(2ⁿ)**    | Tempo exponencial | Força bruta                  |

---

## 🚀 Exemplo de Complexidade O(n)

Este exemplo percorre a lista para verificar se um determinado elemento está presente, resultando em complexidade **O(n)**.

```java
import java.util.List;

public class BuscaElemento {
    public static boolean busca(List<Integer> lista, int elemento) {
        for (int item : lista) {
            if (item == elemento) {
                return true;
            }
        }
        return false;
    }

    public static void main(String[] args) {
        List<Integer> numeros = List.of(1, 2, 3, 4, 5);
        System.out.println(busca(numeros, 3));  // true
    }
}
```

📌 O tempo de execução cresce proporcionalmente ao tamanho da lista.
