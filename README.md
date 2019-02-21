# contains-obj
一个对象包含另一个对象的方法

const arr = [
    { a: 1 },
    { a: 2, b: 1, c: 4 },
    { a: 3, b: 2, c: 5 }
];
const obj = { a: 2, b: 1 };

function where(arr, obj) {
      const keys = Object.keys(obj);
      return arr.filter(item => {
          return keys.every(key => {
              return item[key] && item[key] === obj[key];
          })
      });
  }

console.log(where(arr, obj));  // [{ a: 2, b: 1, c: 4}]
