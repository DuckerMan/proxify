### Proxify
<i>A pretty shitty proxy parser for Rust</i>

### How to use?

Put proxify in your dependency section:

```toml
proxify = "0.3"
```

Use it:

```rust
let proxy = proxify::get_proxy().await;
println!("{:?}", proxy);
```

Also, you can check proxies, duration is time for waiting before we close the connection:

```rust
use std::time::Duration;
let working = check_proxies(&proxy, Duration::from_secs(2)).await;
println!("{:?}", working);
```