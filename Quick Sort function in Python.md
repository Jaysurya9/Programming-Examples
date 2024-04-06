# Python Quick Sort Function

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
