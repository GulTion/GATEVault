---
title: Some Notes must write on paper
allDay: true
date: 2023-09-14
completed: false
---

# CD
## Parsing

### DCFL and Parser relation #notes/cd/parser 
Notable Points:

1. LR(0) ⊂ LR(1) = LR(2) = LR(K), note this is not true for LL(k) grammars 
2. LR(0) set of Grammars is equivalent with Set of All DCFL that is having Prefix Property. (Prefix Property: This is a property which says that let L1 be a string and belongs to your Language then no other Prefix of this string in this language)
3. LR(1) set of Languages are equivalent to Set of all DCFL languages.

### Classification
![[Pasted image 20230914124615.png]]

### Viable Preix
![[Pasted image 20230914140153.png]]

### Number of Steps Taken by bottom up parser with n length token string
![[Pasted image 20230914141240.png]]


#  Sorting #notes/sorting 
## Bubble Sort

![Bubble Sort](https://cdn.emre.me/sorting/bubble_sort.gif)

### Implementation

```python
def bubble_sort(array):
    # We set swapped to True so the loop runs at least once
    swapped = True

    while swapped:
        swapped = False
        for i in range(len(array) - 1):
            if array[i] > array[i + 1]:
                # Swap the elements
                array[i], array[i + 1] = array[i + 1], array[i]
                # Set the flag to True so we'll loop again
                swapped = True

    return array
```

## Selection Sort

![Selection Sort](https://cdn.emre.me/sorting/selection_sort.gif)

### Implementation

```python
def selection_sort(array):
    for i in range(len(array)):
        # We assume that the first item of the unsorted segment is the smallest
        min_value = i

        for j in range(i + 1, len(array)):
            if array[j] < array[min_value]:
                min_value = j

        # Swap values of the lowest unsorted element with the first unsorted element
        array[i], array[min_value] = array[min_value], array[i]

    return array
```

## Insertion Sort

![Insertion Sort](https://cdn.emre.me/sorting/insertion_sort.gif)

### Implementation

```python
def insertion_sort(array):
    # We assume that the first item is sorted
    for i in range(1, len(array)):
        picked_item = array[i]

        # Reference of the index of the previous element
        j = i - 1

        # Move all items to the right until finding the correct position
        while j >= 0 and array[j] > picked_item:
            array[j + 1] = array[j]
            j -= 1

        # Insert the item
        array[j + 1] = picked_item

    return array
```

## Merge Sort

![Merge Sort](https://cdn.emre.me/sorting/merge_sort.gif)

### Implementation

```python
def merge_sort(array):
    # If the list is a single element, return it
    if len(array) <= 1:
        return array

    mid = len(array) // 2

    # Recursively sort and merge each half
    l_list = merge_sort(array[:mid])
    r_list = merge_sort(array[mid:])

    # Merge the sorted lists into a new one
    return _merge(l_list, r_list)


def _merge(l_list, r_list):
    result = []
    l_index, r_index = 0, 0

    for i in range(len(l_list) + len(r_list)):
        if l_index < len(l_list) and r_index < len(r_list):

            # If the item at the beginning of the left list is smaller, add it to the sorted list
            if l_list[l_index] <= r_list[r_index]:
                result.append(l_list[l_index])
                l_index += 1

            # If the item at the beginning of the right list is smaller, add it to the sorted list
            else:
                result.append(r_list[r_index])
                r_index += 1

        # If we have reached the end of the of the left list, add the elements from the right list
        elif l_index == len(l_list):
            result.append(r_list[r_index])
            r_index += 1

        # If we have reached the end of the of the right list, add the elements from the left list
        elif r_index == len(r_list):
            result.append(l_list[l_index])
            l_index += 1

    return result
```

## Heap Sort

![Heap Sort](https://cdn.emre.me/sorting/heap_sort.gif)

### Implementation

```python
def get_left_child(i):
    return 2 * i + 1


def get_right_child(i):
    return 2 * i + 2


def max_heapify(arr, n, i):
    left = get_left_child(i)
    right = get_right_child(i)
    largest = i

    if left < n and arr[left] > arr[largest]:
        largest = left
    if right < n and arr[right] > arr[largest]:
        largest = right
    if largest != i:
        arr[i], arr[largest] = arr[largest], arr[i]
        max_heapify(arr, n, largest)


def heap_sort(arr):
    n = len(arr)

    # build the max heap
    for i in range(n, -1, -1):
        max_heapify(arr, n, i)

    # extract elements one by one
    for i in range(n - 1, 0, -1):
        arr[i], arr[0] = arr[0], arr[i]
        max_heapify(arr, i, 0)

    return arr
```


```
import heapq

def heap_sort(array):
    h = []
    for value in array:
        heapq.heappush(h, value)
    return [heapq.heappop(h) for i in range(len(h))]
```



## Time Complexities of Sorting Algorithms


|Algorithm|Time Complexity (**Best**)|Time Complexity (**Average**)|Time Complexity (**Worst**)|Space Complexity|
|---|---|---|---|---|
|Bubble Sort|O(n)|O(n2)|O(n2)|O(1)|
|Selection Sort|O(n2)|O(n2)|O(n2)|O(1)|
|Insertion Sort|O(n)|O(n2)|O(n2)|O(1)|
|Merge Sort|O(n log(n))|O(n log(n))|O(n log(n))|O(n)|
|Heap Sort|O(n log(n))|O(n log(n))|O(n log(n))|O(1)|
|Quick Sort|O(n log(n))|O(n log(n))|O(n2)|O(log(n))|
|Radix Sort|O (nk)|O(nk)|O(nk)|O(n+k)|
|Tim Sort|O(n)|O(n log(n))|O(n log(n))|O(n)|


# TOC
## DECIDABILITY
![[Pasted image 20230914163632.png]]


<math xmlns="http://www.w3.org/1998/Math/MathML" display="block">
  <mstyle mathsize="0.7em">
    <mtable columnalign="left center center center center center center center" columnspacing="1em" rowspacing="4pt" columnlines="solid solid solid solid solid solid solid" rowlines="solid solid solid solid solid solid solid solid solid solid" frame="solid">
      <mtr>
        <mtd>
          <mtext>Problem</mtext>
        </mtd>
        <mtd>
          <mtext>RL</mtext>
        </mtd>
        <mtd>
          <mtext>DCFL</mtext>
        </mtd>
        <mtd>
          <mtext>CFL</mtext>
        </mtd>
        <mtd>
          <mtext>CSL</mtext>
        </mtd>
        <mtd>
          <mtext>RL</mtext>
        </mtd>
        <mtd>
          <mtext>REL</mtext>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is</mtext>
          <mtext>&#xA0;</mtext>
          <mi>w</mi>
          <mo>&#x2208;</mo>
          <mi>L</mi>
          <mo>?</mo>
          <mtext>(Membership problem)</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is</mtext>
          <mtext>&#xA0;</mtext>
          <mi>L</mi>
          <mo>=</mo>
          <mi>&#x3D5;</mi>
          <mo>?</mo>
          <mtext>(Emptiness problem)</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is</mtext>
          <mtext>&#xA0;</mtext>
          <mi>L</mi>
          <mo>=</mo>
          <msup>
            <mi mathvariant="normal">&#x3A3;</mi>
            <mo>&#x2217;</mo>
          </msup>
          <mo>?</mo>
          <mtext>(Completeness problem)</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is</mtext>
          <mtext>&#xA0;</mtext>
          <msub>
            <mi>L</mi>
            <mn>1</mn>
          </msub>
          <mo>=</mo>
          <msub>
            <mi>L</mi>
            <mn>2</mn>
          </msub>
          <mo>?</mo>
          <mtext>(Equality problem)</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is</mtext>
          <mtext>&#xA0;</mtext>
          <msub>
            <mi>L</mi>
            <mn>1</mn>
          </msub>
          <mo>&#x2286;</mo>
          <msub>
            <mi>L</mi>
            <mn>2</mn>
          </msub>
          <mo>?</mo>
          <mtext>(Subset problem)</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is&#xA0;</mtext>
          <msub>
            <mi>L</mi>
            <mn>1</mn>
          </msub>
          <mo>&#x2229;</mo>
          <msub>
            <mi>L</mi>
            <mn>2</mn>
          </msub>
          <mo>=</mo>
          <mi>&#x3D5;</mi>
          <mo>?</mo>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is L finite? (finiteness problem)</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is complement of &#x2018;L' a language of the same class?</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is intersection of two languages of the same class?</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
      </mtr>
      <mtr>
        <mtd>
          <mtext>Is L a regular Language?</mtext>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
        <mtd>
          <mi>U</mi>
          <mi>D</mi>
        </mtd>
      </mtr>
    </mtable>
  </mstyle>
</math>


## UA NOTES for DECIDABITY




