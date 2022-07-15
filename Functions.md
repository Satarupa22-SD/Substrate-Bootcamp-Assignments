```
//Question:
//1.🌟🌟🌟

fn main() {
    // Don't modify the following two lines!
    let (x, y) = (1, 2);
    let s = sum(x, y);

    assert_eq!(s, 3);

    println!("Success!");
}

fn sum(x, y: i32) {
    x + y;
}
//_______________________________________________________________________________________________________________________________________________________________________
//Solution:
fn main() {
    // Don't modify the following two lines!
    let (x, y) = (1, 2);
    let s = sum(x, y);

    assert_eq!(s, 3);

    println!("Success!");
}

fn sum(x: i32, y: i32)->i32 {
    x + y
}
//_____________________________________________________________________________________________________________________________________________________________________
//Question:
//2. 🌟
fn main() {
   print();
}

// Replace i32 with another type
fn print() -> i32 {
   println!("Success!");
}
//_____________________________________________________________________________________________________________________________________________________________________
//Soluton:
fn main() {
   print();
}

// Replace i32 with another type
fn print() -> () {
   println!("Success!");
}
//_____________________________________________________________________________________________________________________________________________________________________
//Question:
//3. 🌟
// Solve it in two ways
// DON'T let `println!` works
fn main() {
    never_return();

    println!("Failed!");
}

fn never_return() -> ! {
    // Implement this function, don't modify the fn signatures
    
}
c
fn main() {
    never_return();
}

fn never_return() -> ! {
    // implement this function, don't modify fn signatures
    panic!("I return nothing!")
}
//_____________________________________________________________________________________________________________________________________________________________________
//Question:
//4. 🌟
fn main() {
    println!("Success!");
}

fn get_option(tp: u8) -> Option<i32> {
    match tp {
        1 => {
            // TODO
        }
        _ => {
            // TODO
        }
    };
    
    // Rather than returning a None, we use a diverging function instead
    never_return_fn()
}

// IMPLEMENT this function in THREE ways
fn never_return_fn() -> ! {
    
}
:
