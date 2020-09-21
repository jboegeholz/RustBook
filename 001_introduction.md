# Rust for Pythonistas

Rust is a comparably young language. It was first presented in 2010 but a stable version jsut came out in 2015.

## Hello World
Let's start with the classic: Hello world

<table>
<thead>
<tr>
<th>Python</th>
<th>Rust</th>
</tr>
</thead>
<tbody>
<tr><td>
<pre>print("Hello Python")</pre>
</td>
<td>
<pre>fn main() {
    println!("Hello Rust!");
}</pre>
</td></tr>
</tbody>
</table>

## Main function
Every Rust program starts inside a main function:
<pre>fn main() {
    // your code goes here
}</pre>

which in Python is normally achieved via
<pre>
def main():
    pass


if __name__ == '__main__':
    main()
</pre>
(Which is a good practice to use, but not mandatory)

Another thing you might notice is the return of the curly brackets and semicolons :-)

## Print functions
The println! is a so called macro



