def lmis(array):
    n = len(array)
    dp = [1] * n  #panjang LMIS
    previous = [-1] * n  #melacak jalur
    
    #menghitung panjang LMIS
    for i in range(1, n):
        for j in range(i):
            if array[j] <= array[i] and dp[i] < dp[j] + 1:
                dp[i] = dp[j] + 1
                previous[i] = j

    #panjang maksimum dan jalur
    max_length = max(dp)
    end_index = dp.index(max_length)
    path = []
    
    while end_index != -1:
        path.append(array[end_index])
        end_index = previous[end_index]
    path.reverse()  #urutan jalur awal - akhir
    
    return max_length, path

def main():
    print("Masukkan tinggi daun yang berada di depan Timmy dalam sentimeter:")
    user_input = input()
    array = list(map(int, user_input.split()))
    max_length, path = lmis(array)

    print(f"Timmy melompati dedaunan dengan tinggi: {path}")
    print(f"Panjang jalur lompatan Timmy: {max_length}")


if __name__ == "__main__":
    main()
