# Explicação do Código: Verificação de Número Primo

## Código

```python
def is_prime(n):
    """
    Verifica se um número é primo.
    
    Args:
        n (int): O número a ser verificado.
    
    Returns:
        bool: True se o número for primo, False caso contrário.
    """
    if n <= 1:
        return False
    if n == 2:
        return True
    if n % 2 == 0:
        return False
    for i in range(3, int(n**0.5) + 1, 2):
        if n % i == 0:
            return False
    return True

if __name__ == "__main__":
    # Testes simples
    print(is_prime(2))  # True
    print(is_prime(3))  # True
    print(is_prime(4))  # False
    print(is_prime(17)) # True
    print(is_prime(18)) # False
```

## Explicação Linha a Linha

1. `def is_prime(n):` - Define a função chamada `is_prime` que recebe um parâmetro `n` (o número a ser verificado).

2. `"""` - Início da docstring, que é a documentação da função em Python.

3. `Verifica se um número é primo.` - Descrição geral da função.

4.  - Linha em branco para formatação.

5. `Args:` - Seção que descreve os argumentos da função.

6. `    n (int): O número a ser verificado.` - Especifica que `n` é um inteiro que representa o número a verificar.

7.  - Linha em branco.

8. `Returns:` - Seção que descreve o valor de retorno.

9. `    bool: True se o número for primo, False caso contrário.` - Indica que a função retorna um booleano.

10. `"""` - Fim da docstring.

11. `if n <= 1:` - Verifica se o número `n` é menor ou igual a 1.

12. `    return False` - Se for, retorna `False`, pois números ≤ 1 não são primos.

13. `if n == 2:` - Verifica se `n` é exatamente 2.

14. `    return True` - Retorna `True`, pois 2 é o único número primo par.

15. `if n % 2 == 0:` - Verifica se `n` é divisível por 2 (ou seja, se é par).

16. `    return False` - Se for par e maior que 2, retorna `False`, pois não é primo.

17. `for i in range(3, int(n**0.5) + 1, 2):` - Inicia um loop que itera sobre números ímpares de 3 até a raiz quadrada de `n` (inclusive), pulando de 2 em 2.

18. `    if n % i == 0:` - Dentro do loop, verifica se `n` é divisível por `i`.

19. `        return False` - Se for divisível, retorna `False`, indicando que não é primo.

20. `return True` - Se o loop terminar sem encontrar divisores, retorna `True`, confirmando que é primo.

21.  - Linha em branco.

22. `if __name__ == "__main__":` - Verifica se o script está sendo executado diretamente (não importado como módulo).

23. `    # Testes simples` - Comentário indicando que seguem testes.

24. `    print(is_prime(2))  # True` - Chama a função com 2 e imprime o resultado (esperado: True).

25. `    print(is_prime(3))  # True` - Chama com 3 (True).

26. `    print(is_prime(4))  # False` - Chama com 4 (False).

27. `    print(is_prime(17)) # True` - Chama com 17 (True).

28. `    print(is_prime(18)) # False` - Chama com 18 (False).