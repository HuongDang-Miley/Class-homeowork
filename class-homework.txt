// Classes Homework
// Take the instructions below, paste them into a .js file, comment them out, and complete the exercise.
// When finished, upload the .js file

// 1. Create a Student and a Classroom Class
class Student {
    // 2. When the class is instantiated it should have a name, favoriteSubject, and gpa variable into which we can pass values during instantiation
    constructor(name, favoriteSubject, gpa) {
        this.name = name;
        this.favoriteSubject = favoriteSubject;
        this.gpa = gpa;
    }

    // 3. Also create a studentDescribe method where if name is 'Joe' favoriteSubject is 'science' and gpa is 4.0' the method should log: 'Joe favorite subject is science. Joe has a gpa of 4.0.
    studentDescribe() {
        console.log(`${this.name} favorite subject is ${this.favoriteSubject} and GPA is ${this.gpa}`)
    }
}

// 4. In your Classroom class:
class Classroom {
    // a. Create an empty array where we can add students
    // b. Create a professor and roomNumber property
    constructor(professor, roomNumber) {
        this.students = [];
        this.professor = professor;
        this.roomNumber = roomNumber;
    }

    // 5. Create a classDescribe method
    classDescribe() {
        // a. Method should print information
        // b. If the arguments for a new instance of Classroom are ‘Professor Johnson’ for professor, 417 for the roomNumber and the number of students is 12 should log: "Professor Johnson's class is in room 417. Professor Johnson has 12 students"
        console.log(`${this.professor}'s class is in the room ${this.roomNumber}. ${this.professor} has ${this.students.length} students`)    
    }

    // 6. create a method called addStudent that can add a student to the students array
    addStudent(name){
        this.students.push(name)
        return this
    }

    // 7. create a studentCount method that if, for example, there are 5 students, will log: 'There are 5 students in the class'
    studentCount(){
        console.log(`There are ${this.students.length} students in the class`)
        return this
    }

    // 8. create a method called studentNames in the Classroom class. It should log each name of the students in the classroom one by one.
    studentNames(){
        for (const student of this.students){
            console.log(student)
        }
        return this
    }
}

// Create two new Student instances and give them values. They should be called called student1 and student2
const student1 = new Student('student1', 'Accounting', 3.75)
const student2 = new Student('student2', 'Chinese', 3.5)


// 9. Describe each student by logging them with your method.
student1.studentDescribe()
student2.studentDescribe()


// 10. Create a new Classroom instance called firstClass and add values.
const firstClass = new Classroom('Professor Johnson', 417)


// 11. Add the two students to the new classroom
firstClass.addStudent(student1)
firstClass.addStudent(student2)


// 12. Use your method to describe the class
firstClass.classDescribe()


// 13. change the name of student one to Peter using your instantiated student2
student2.name = 'Peter'


// 14. Call firstClass and chain the studentCount and studentNames methods
firstClass.studentCount().studentNames()