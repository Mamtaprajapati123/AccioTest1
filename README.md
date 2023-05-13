# AccioTest1
let arr = [
  { id: 1, name: "john", age: "18", marks: 80 },
  { id: 2, name: "jack", age: "20", marks: 85 },
  { id: 3, name: "karen", age: "19", marks: 35 }
];

function PrintStudentswithMap() {
  const filteredArr = arr.filter(student => student.marks > 50);
  const mappedArr = filteredArr.map(student => {
    return {
      id: student.id,
      name: student.name,
      age: student.age,
      marks: student.marks
    };
  });
  console.log(mappedArr);
}

function PrintStudentsbyForEach() {
  const filteredArr = [];
  arr.forEach(student => {
    if (student.marks > 50) {
      filteredArr.push(student);
    }
  });
  console.log(filteredArr);
}

function addData() {
  const newStudent = { id: 4, name: "susan", age: "20", marks: 45 };
  arr.push(newStudent);
  console.log(arr);
}

function removeFailedStudent() {
  const filteredArr = arr.filter(student => student.marks >= 50);
  console.log(filteredArr);
}

function concatenateArray() {
  const newArr = [
    { id: 4, name: "alice", age: "21", marks: 90 },
    { id: 5, name: "bob", age: "19", marks: 75 },
    { id: 6, name: "charlie", age: "20", marks: 60 }
  ];
  const concatenatedArr = arr.concat(newArr);
  console.log(concatenatedArr);
}
