# Quest-for-Champion-Numbers

In a distant land, Riya has an array of size N, filled with magical numbers. She’s on a quest to find the "Champion Elements" in her array. A Champion Element is a number that has no larger number to its right.
More precisely, a number at position i where (0 ≤ i < N) is a Champion Element if there is no number at any position j, where (i < j < N) that is greater than the number at position i.
Can you help Riya count the number of Champion Elements in her array?

def count_champion_elements(arr):

    n = len(arr)
    max_right = -1  
    champion_count = 0

    for i in range(n - 1, -1, -1):
        if arr[i] >= max_right:
            champion_count += 1  
            max_right = arr[i]   

    return champion_count

n = int(input())           
arr = list(map(int, input().split()))  

print(count_champion_elements(arr))
