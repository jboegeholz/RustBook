## Random Numbers

<pre>use rand::Rng;

fn main() {
    for _i in 0..10 {
        let random_number = rand::thread_rng().gen_range(1, 101);
        println!("{}", random_number);
    }
}</pre>