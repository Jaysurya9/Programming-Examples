# Quick Sort Function in Python

    def quick_sort(data):
      """
      Sorts a list of data in ascending order using the Quick Sort algorithm.
      Args:
          data: A list of data to be sorted.
      Returns:
          A new list containing the sorted data.
      """
      if len(data) <= 1:
        return data
      pivot = data[0]
      left = [i for i in data[1:] if i <= pivot]
      right = [i for i in data[1:] if i > pivot]
    
      return quick_sort(left) + [pivot] + quick_sort(right)
    
    # Example usage
    data = [8, 3, 1, 4, 2, 7, 6, 5]
    sorted_data = quick_sort(data)
    print(sorted_data)  # Output: [1, 2, 3, 4, 5, 6, 7, 8]

# Bubble Sort Function in Python

    def bubble_sort(data):
      """
      Sorts a list of data in ascending order using the Bubble Sort algorithm.
      Args:
          data: A list of data to be sorted.
      Returns:
          A new list containing the sorted data.
      """
      # Iterate through the list n-1 times
      for i in range(len(data) - 1):
        # Swap elements if they are in the wrong order
        for j in range(len(data) - i - 1):
          if data[j] > data[j + 1]:
            data[j], data[j + 1] = data[j + 1], data[j]
    
      return data
    
    # Example usage
    data = [8, 3, 1, 4, 2, 7, 6, 5]
    sorted_data = bubble_sort(data)
    print(sorted_data)  # Output: [1, 2, 3, 4, 5, 6, 7, 8]
