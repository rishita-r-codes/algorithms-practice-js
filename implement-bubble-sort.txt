** start of script.js **

function bubbleSort(array) {
  // Only change code below this line
  let sorted = false;
  while (!sorted) {
    let noSwaps = 0;
    for (let i = 0; i < array.length - 1; i++) {
      if (array[i] > array[i+1]) {
        let temp = array[i];
        array[i] = array[i+1];
        array[i+1] = temp;
      }
      else {
        noSwaps++;
      }
      if (noSwaps >= array.length - 1) {
        sorted = true;
      }
    }
  }
  return array;
  // Only change code above this line
}


** end of script.js **

