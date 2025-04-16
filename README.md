function bubbleSort(arr) {
  let n = arr.length;
  let swapped;

  do {
    swapped = false;
    for (let i = 0; i < n - 1; i++) {
      if (arr[i] > arr[i + 1]) {
        // Troca os elementos
        [arr[i], arr[i + 1]] = [arr[i + 1], arr[i]];
        swapped = true;
      }
    }
    n--; 
  } while (swapped);

  return arr;
}

const array = [97, 45, 49, 32, 2, 5, 9, 99, 1, 7];
console.log("Original:", array);
const sorted = bubbleSort(array);
console.log("Ordenado:", sorted);
