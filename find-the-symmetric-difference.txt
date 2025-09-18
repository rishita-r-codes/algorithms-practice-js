** start of script.js **

function sym(...args) {

  function symDiff(arg1, arg2) {
    let new1 = arg1.filter((element) => !arg2.includes(element))
    let new2 = arg2.filter((element) => !arg1.includes(element))
    return new1.concat(new2);
  }
  
  return [...new Set(args.reduce(symDiff))];
}

console.log(sym([1, 2, 3, 3], [5, 2, 1, 4]));



** end of script.js **

