## Variables

There is a big difference between Python and Rust reagrding variables:
Rust has immutable variables and they are the default behaviour.

<table><thead>
<tr><th>Python</th><th>Rust</th></tr>
</thead>
<tbody>
<tr><td><pre>my_age = 39</pre></td><td><pre>let my_age:i32 = 39;</pre></td></tr>
</tbody>
</table>

While in Python you can now change the age to any other number or even let the variable "point" to an instance of another data type
in Rust the age is fixed. Which would be really lovely *fg*

To make a variable changeable in Rust you apply the keyword "mut" which stands for mutable.
<pre>let mut my_age:i32 = 39;</pre>

The :i32 can be ommited because Rust can infer the type from the value given at declaration.
But explicit is always better than implicit. 