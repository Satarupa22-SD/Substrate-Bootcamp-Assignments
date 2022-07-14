``` Binding and mutability

Question:

// 1. 🌟 Fix the error below with least amount of modification to the code

fn main() {
    let x: i32; // Uninitialized but used, ERROR !
    let y: i32; // Uninitialized but also unused, only a Warning !

    assert_eq!(x, 5);
    println!("Success!");
} 


//_____________________________________________________________________________________________________________________________________________________________________

//Solution:


// Fix the error below with least amount of modification to the code
fn main() {
    let x: i32 = 5; // Uninitialized but used, ERROR !
    let y: i32; // Uninitialized but also unused, only a Warning !

    assert_eq!(x, 5);
    println!("Success!");
}

_______________________________________________________________________________________________________________________________________________________________________
//2. 🌟 Use mut to mark a variable as mutable.


// Fill the blanks in the code to make it compile
fn main() {
    let __ =  1;
    __ += 2; 
    
    assert_eq!(x, 3);
    println!("Success!");
}
//_______________________________________________________________________________________________________________________________________________________________________
Solution:
// Fill the blanks in the code to make it compile
fn main() {
    let mut x =  1;
    x += 2; 
    
    assert_eq!(x, 3);
    println!("Success!");
}
//_____________________________________________________________________________________________________________________________________________________________________

// A scope is the range within the program for which the item is valid.

3. 🌟
Question:

// Fix the error below with least amount of modification
fn main() {
    let x: i32 = 10;
    {
        let y: i32 = 5;
        println!("The value of x is {} and value of y is {}", x, y);
    }
    println!("The value of x is {} and value of y is {}", x, y); 
}
//_____________________________________________________________________________________________________________________________________________________________________

Solution:

// Fix the error below with least amount of modification
fn main() {
    let x: i32 = 10;
    
        let y: i32 = 5;
        println!("The value of x is {} and value of y is {}", x, y);
    }
    
//_____________________________________________________________________________________________________________________________________________________________________

//Question:
// 4. 🌟🌟

// Fix the error with the use of define_x
fn main() {
    println!("{}, world", x); 
}

fn define_x() {
    let x = "hello";
}

//_____________________________________________________________________________________________________________________________________________________________________

//Solution:

fn main() {
    let x = define_x();
    println!("{}, world", x);
}

fn define_x() -> String {
    let x = "hello".to_string();
    x
}

//_____________________________________________________________________________________________________________________________________________________________________

//Question:

//You can declare a new variable with the same name as a previous variable, here we can say **the first one is shadowed by the second one.

5.🌟🌟

// Only modify `assert_eq!` to make the `println!` work(print `42` in terminal)
fn main() {
    let x: i32 = 5;
    {
        let x = 12;
        assert_eq!(x, 5);
    }

    assert_eq!(x, 12);

    let x =  42;
    println!("{}", x); // Prints "42".
}
//_____________________________________________________________________________________________________________________________________________________________________
//Solution:

// Only modify `assert_eq!` to make the `println!` work(print `42` in terminal)
fn main() {
    let x: i32 = 5;
    {
        let x = 12;
        assert_eq!(x, 12);
    }

    assert_eq!(x, 5);

    let x =  42;
    println!("{}", x); // Prints "42".
}
//_____________________________________________________________________________________________________________________________________________________________________
//Question:
//6.🌟🌟

// Remove a line in the code to make it compile
fn main() {
    let mut x: i32 = 1;
    x = 7;
    // Shadowing and re-binding
    let x = x; 
    x += 3;


    let y = 4;
    // Shadowing
    let y = "I can also be bound to text!"; 

    println!("Success!");
}
//_____________________________________________________________________________________________________________________________________________________________________

//Solution:

// Remove a line in the code to make it compile
fn main() {
    let mut x: i32 = 1;
    x = 7;
    // Shadowing and re-binding
     
    x += 3;


    let y = 4;
    // Shadowing
    let y = "I can also be bound to text!"; 

    println!("Success!");
}
//_____________________________________________________________________________________________________________________________________________________________________

// Question:
// 7. 🌟 unused variable :

fn main() {
    let x = 1; 
}

// Warning: unused variable: `x`

//_____________________________________________________________________________________________________________________________________________________________________

//Solution:

fn main() {
    let x = 1; 
    
    println!("{}",x);
}

//_____________________________________________________________________________________________________________________________________________________________________

//Question:
//8. 🌟🌟 We can use a pattern with let to destructure a tuple to separate variables.


// Fix the error below with least amount of modification
fn main() {
    let (x, y) = (1, 2);
    x += 2;

    assert_eq!(x, 3);
    assert_eq!(y, 2);

    println!("Success!");
}

//_____________________________________________________________________________________________________________________________________________________________________
//Solution:

// Fix the error below with least amount of modification
fn main() {
    let (mut x, mut y) = (1, 2);
    x += 2;

    assert_eq!(x, 3);
    assert_eq!(y, 2);

    println!("Success!");
}





