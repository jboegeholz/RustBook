## Traits

struct Parent {
    function: &'static str,
    parent_name: &'static str,
}

impl Display for Parent{
    fn fmt (&self, fmt: &mut std::fmt::Formatter) -> std::result::Result<(), std::fmt::Error> {
        write!(fmt, "I'm your {} Luke, you can call me {}", self.function, self.parent_name)
    }
}



Traits are like protocols
```
trait Animal {
    fn name(&amp;self) -&gt; &amp;'static str;

   fn talk(&amp;self){
        println!("{} cannot talk", self.name());
    }
}
struct Human{
    name: &amp;'static str
}

impl Animal for Human
{
    fn name(&amp;self) -&gt; &amp;'static str{
        self.name
    }
    fn talk(&amp;self){
        println!("Hello my name is {}", self.name);
    }
}
fn traits() {
    let h = Human{name:"John"};
    h.talk();
} ```