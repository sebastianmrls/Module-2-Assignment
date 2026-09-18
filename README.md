# Module-2-Assignment-Solution
  To analize the Big O of getLargest() method, I first defined n as the size of the array.

    n = sz

  The main operation I focused on was

    int product = arr[iterate1] * arr[iterate2];

  This line is repeated while iterate1 stays on one element and iterate2 moves through all the elements that come after it

  For example, if:

    arr = {2, 4, 6, 8}
    n = 4

  The algorithm calculates:

    2 * 4
    2 * 6
    2 * 8

    4 * 6
    4 * 8

    6 * 8

  In general, the number of product calculations is:

    (n−1) + (n−2) + (n−3) + ... + 2 + 1

  This is the same triangular pattern discussed in the class materials, where each new pass has one fewer in comparison to the previous one

  Using the sum formula:

    1 + 2 + 3 + ... + (n−1) = n(n-1)/2

  Expanding:

    n^2 - n / 2

  For Big O, I keep the fastest-growing term and ignore constants and lower-order terms
  
  The fastest-growing term is:

    n^2 (n squared)

  Therefore, the time complexity of the method is:

    O(n^2)
  
  ​
