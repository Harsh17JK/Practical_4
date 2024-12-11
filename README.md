# Function to perform Insertion Sort
def insertionSort(arr):
    n = len(arr)  # Get the length of the array
    if n <= 1:
        return  # If the array has 0 or 1 element, it is already sorted, so return
    
    # Iterate over the array starting from the second element
    for i in range(1, n):
        key = arr[i]  # Store the current element as the key to be inserted
        j = i - 1
        while j >= 0 and key < arr[j]:  # Move elements greater than key one position ahead
            arr[j + 1] = arr[j]  # Shift elements to the right
            j -= 1
        arr[j + 1] = key  # Insert the key in the correct position

# Sorting the array [12, 11, 13, 5, 6] using insertionSort
arr = [12, 11, 13, 5, 6]
print("Array before Sorting:")
print(arr)
print()

insertionSort(arr)
print("Array after sorting using Insertion Sort:")
print(arr)
print()

# Function to perform Shell Sort
def shellSort(arr):
    n = len(arr)
    gap = n // 2  # Start with a big gap, then reduce the gap
    # Do a gapped insertion sort for this gap size
    while gap > 0:
        for i in range(gap, n):
            temp = arr[i]  # Save a[i] in temp and make a hole at position i
            j = i
            # Shift earlier gap-sorted elements up until the correct location for a[i] is found
            while j >= gap and arr[j - gap] > temp:
                arr[j] = arr[j - gap]
                j -= gap
            arr[j] = temp  # Put temp (the original a[i]) in its correct location
        gap //= 2  # Reduce the gap size

# Driver code to test the above functions
arr = [12, 34, 54, 2, 3]
print("Array before sorting:")
print(arr)
shellSort(arr)
print("\nArray after sorting using Shell Sort:")
print(arr)
print()

# Extracting the top 5 elements
top5 = []
for i in range(-5, 0):  # Extract the top 5 elements from the sorted array
    top5.append(arr[i])

print("Top 5 elements:", top5)
