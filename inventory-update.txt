** start of script.js **

function updateInventory(arr1, arr2) {
    for (let i=0; i<arr2.length; i++) {
        let index = arr1.findIndex((record) => record[1]===arr2[i][1])
        if (index === -1) {
            arr1.push(arr2[i])
        }
        else {
            arr1[index][0] += arr2[i][0]
        }
        
    }
    return arr1.sort((a,b) => a[1].localeCompare(b[1]))
    
}

// Example inventory lists
var curInv = [
    [21, "Bowling Ball"],
    [2, "Dirty Sock"],
    [1, "Hair Pin"],
    [5, "Microphone"]
];

var newInv = [
    [2, "Hair Pin"],
    [3, "Half-Eaten Apple"],
    [67, "Bowling Ball"],
    [7, "Toothpaste"]
];

updateInventory(curInv, newInv);

** end of script.js **

