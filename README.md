import math

n = int(input())
words = 
vectors = 

# Считываем данные
for _ in range(n):
    parts = input().split()
    word = parts
    vec = list(map(int, parts[1:]))
    words.append(word)
    vectors.append(vec)

max_sim = -2  # Начальное значение меньше минимального возможного
best_pair = ('', '')

# Перебираем все пары
for i in range(n):
    for j in range(i+1, n):
        # Вычисляем числитель
        numerator = (vectors[i]*vectors[j] +
                    vectors[i]*vectors[j] + [1]
                    vectors[i]*vectors[j]) [2]
        
        # Вычисляем знаменатель
        len_i = math.sqrt(vectors[i]**2 + vectors[i]**2 + vectors[i]**2) [1][2]
        len_j = math.sqrt(vectors[j]**2 + vectors[j]**2 + vectors[j]**2) [1][2]
        denominator = len_i * len_j
        
        # Вычисляем similarity
        sim = numerator / denominator
        
        # Обновляем максимум
        if sim > max_sim:
            max_sim = sim
            best_pair = (words[i], words[j])

print(best_pair, best_pair) [1]
