## Loops

### For-Loops
<table>
<thead>
<tr>
<th>Python</th>
<th>Rust</th>
</tr>
</thead>
<tbody>
<tr><td>
<pre>
for count in range(1, 565):
    print(count)
</pre>
</td>
<td>
<pre>
for count in 1..565 {
    println!("{}", count);
}
</pre>
</td></tr>
</tbody>
</table>
Loops are even easier as in Python! Rust uses a modern range syntax with start . . stop

#### Value and position -> enumerate
<table>
<thead>
<tr>
<th>Python</th>
<th>Rust</th>
</tr>
</thead>
<tbody>
<tr><td>
<pre>
for child_no, age in enumerate(range(30, 41)):
    print(f"Got our {child_no+1}. child with {age}")
</pre>
</td>
<td>
<pre>
    for (child_no, age) in (30..41).enumerate(){
        println!("Got our {}. child with {}", child_no+1, age);
    }
</pre>
</td></tr>
</tbody>
</table>

### While-Loops

<table>
<thead>
<tr>
<th>Python</th>
<th>Rust</th>
</tr>
</thead>
<tbody>
<tr><td>
<pre>
grey_hairs = 1
while dads_grey_hairs < 1000:
    dads_grey_hairs *= 2
    print(f"Dad has {dads_grey_hairs} hairs")
</pre>
</td>
<td>
<pre>
    let mut dads_grey_hairs = 1;
    while dads_grey_hairs < 1000 {
        dads_grey_hairs *= 2;
        println!("Dad has {} grey hairs", dads_grey_hairs);
    }
</pre>
</td></tr>
</tbody>
</table>

### Loop-Loop
<pre>
    let mut moms_grey_hairs = 1;
    loop {
        moms_grey_hairs *= 2;
        println!("Mom has {} grey hairs", moms_grey_hairs);
        if moms_grey_hairs == 1<<10 { break; }
    }
</pre>