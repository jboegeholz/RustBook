## match
<pre>
    let country_code = 44;
    let country = match country_code {
        44 => "UK",
        46 => "Sweden",
        _ => "unknown"
    };
    println!("{} {}", country_code, country);
</pre>