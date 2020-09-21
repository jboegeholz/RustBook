## Modules

<table>
<thead>
<tr>
<th>Python</th>
<th>Rust</th>
</tr>
</thead>
<tbody>
<tr><td>
person.py
<pre>
class Person:
    def __init__(self, age):
        self.age = age
</pre>
</td>
<td>
person.rs
<pre>pub struct Person {
    pub age: i32,
}</pre>
</td></tr>
<tr><td>
main.py
<pre>
from person import Person
dad = Person(age=39)
print(dad.age)</pre>
</td>
<td>
main.rs
<pre>
mod person;
use crate::person::Person;
..
fn main(){
    let dad = Person { age: 39, };
    println!("{}", dad.age);
}
</pre>
</td></tr>
</tbody>
</table>