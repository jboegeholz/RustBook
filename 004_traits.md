## Traits

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