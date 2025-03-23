def is_prime(num):
    """Fungsi untuk memeriksa apakah suatu bilangan adalah prima."""
    if num <= 1:
        return False
    for i in range(2, int(num**0.5) + 1):
        if num % i == 0:
            return False
    return True

def find_nearest_prime(n):
    """Fungsi untuk mencari bilangan prima terdekat yang kurang dari n."""
    if n <= 2:
        return "Tidak ada bilangan prima yang kurang dari n."
    
    nearest_prime = 0
    for i in range(n - 1, 1, -1):
        if is_prime(i):
            nearest_prime = i
            break
            
    if nearest_prime:
        return nearest_prime
    else:
        return "Tidak ada bilangan prima yang kurang dari n."
