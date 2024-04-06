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

# Merge Sort in Python

    def merge_sort(data):
      """
      Sorts a list of data in ascending order using the Merge Sort algorithm.
      Args:
          data: A list of data to be sorted.
      Returns:
          A new list containing the sorted data.
      """
      if len(data) <= 1:
        return data
      # Divide the data into two halves
      mid = len(data) // 2
      left = merge_sort(data[:mid])
      right = merge_sort(data[mid:])
    
      # Merge the sorted halves
      return merge(left, right)
    
    def merge(left, right):
      """
      Merges two sorted lists into a single sorted list.
    
      Args:
          left: A sorted list.
          right: A sorted list.
    
      Returns:
          A new list containing the merged and sorted data.
      """
      merged = []
      i = 0
      j = 0
      while i < len(left) and j < len(right):
        if left[i] <= right[j]:
          merged.append(left[i])
          i += 1
        else:
          merged.append(right[j])
          j += 1
    
      # Append remaining elements
      merged += left[i:]
      merged += right[j:]
    
      return merged
    
    # Example usage
    data = [8, 3, 1, 4, 2, 7, 6, 5]
    sorted_data = merge_sort(data)
    print(sorted_data)  # Output: [1, 2, 3, 4, 5, 6, 7, 8]
