````
//Question:
//1.🌟Char

// Make it work
use std::mem::size_of_val;
fn main() {
    let c1 = 'a';
    assert_eq!(size_of_val(&c1),1); 

    let c2 = '中';
    assert_eq!(size_of_val(&c2),3); 

    println!("Success!");
} 
//_______________________________________________________________________________________________________________________________________________________________________
//Solution:

// Make it work
use std::mem::size_of_val;
fn main() {
    let c1 = 'a';
    assert_eq!(size_of_val(&c1),4); 

    let c2 = '中';
    assert_eq!(size_of_val(&c2),4); 

    println!("Success!");
} 
//_____________________________________________________________________________________________________________________________________________________________________
//Quesion:
//2.🌟Char

// Make it work
fn main() {
    let c1 = "中";
    print_char(c1);
} 

fn print_char(c : char) {
    println!("{}", c);
}

//_____________________________________________________________________________________________________________________________________________________________________
//Solution:

// Make it work
fn main() {
    let c1 = '中';
    print_char(c1);
} 

fn print_char(c : char) {
    println!("{}", c);
}

//_____________________________________________________________________________________________________________________________________________________________________
Question:
//3.🌟 Bool

// Make println! work
fn main() {
    let _f: bool = false;

    let t = true;
    if !t {
        println!("Success!");
    }
} 
//_____________________________________________________________________________________________________________________________________________________________________
//Solution:

// Make println! work
fn main() {
    let _f: bool = false;

    let t = false;
    if !t {
        println!("Success!");
    }
} 
//_____________________________________________________________________________________________________________________________________________________________________
Question:
//4.🌟 Bool

// Make it work
fn main() {
    let f = true;
    let t = true && false;
    assert_eq!(t, f);

    println!("Success!");
}

//_____________________________________________________________________________________________________________________________________________________________________
//Solution:

// Make it work
fn main() {
    let f: bool = true;
    let t = true;
    assert_eq!(t, f);

    println!("Success!");
}
//_____________________________________________________________________________________________________________________________________________________________________
Question:
//5.🌟 Unit:

// Make it work, don't modify `implicitly_ret_unit` !
fn main() {
    let _v: () = ();

    let v = (2, 3);
    assert_eq!(v, implicitly_ret_unit());

    println!("Success!");
}

fn implicitly_ret_unit() {
    println!("I will return a ()");
}

// Don't use this one
fn explicitly_ret_unit() -> () {
    println!("I will return a ()");
}

//_____________________________________________________________________________________________________________________________________________________________________
//Solution:
fn main() {
    let v0: () = ();

    let v = (2, 3);
    assert_eq!(v0, implicitly_ret_unit())
}

fn implicitly_ret_unit() {
    println!("I will returen a ()")
}

// don't use this one
fn explicitly_ret_unit() -> () {
    println!("I will returen a ()")
}

//_____________________________________________________________________________________________________________________________________________________________________
Question:
//6.🌟 Unit:

// Modify `4` in assert to make it work
use std::mem::size_of_val;
fn main() {
    let unit: () = ();
    assert!(size_of_val(&unit) == 4);

    println!("Success!");
}

//_____________________________________________________________________________________________________________________________________________________________________
//Solution:

// Modify `4` in assert to make it work
use std::mem::size_of_val;
fn main() {
    let unit: () = ();
    assert!(size_of_val(&unit) == 0);

    println!("Success!");
}
