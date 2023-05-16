## greet_world_challenges

**demo 知识点**

- 控制流：for 和 continue 连在一起使用，实现循环控制。
- 方法语法：由于 Rust 没有继承，因此 Rust 不是传统意义上的面向对象语言，但是它却从 OO 语言那里偷师了方法的使用 record.trim()，record.split(',') 等。
- 高阶函数编程：函数可以作为参数也能作为返回值，例如 .map(|field| field.trim())，这里 map 方法中使用闭包函数作为参数，也可以称呼为 匿名函数、lambda 函数。
- 类型标注：if let Ok(length) = fields[1].parse::<f32>()，通过 ::<f32> 的使用，告诉编译器 length 是一个 f32 类型的浮点数。这种类型标注不是很常用，但是在编译器无法推断出你的数据类型时，就很有用了。
- 条件编译：if cfg!(debug_assertions)，说明紧跟其后的输出（打印）只在 debug 模式下生效。
- 隐式返回：Rust 提供了 return 关键字用于函数返回，但是在很多时候，我们可以省略它。因为 Rust 是 基于表达式的语言。

使用 cargo run

```bash
cargo run
   Compiling greet_world_challage v0.1.0 (/Users/carl/github/rust/rust-course/packages/greet_world_challage)
    Finished dev [unoptimized + debuginfo] target(s) in 0.85s
     Running `target/debug/greet_world_challage`
      debug: "    Little penguin,33" -> ["Little penguin", "33"]
      Little penguin, 33cm
      debug: "    Yellow-eyed penguin,65" -> ["Yellow-eyed penguin", "65"]
      Yellow-eyed penguin, 65cm
      debug: "    Fiordland penguin,60" -> ["Fiordland penguin", "60"]
      Fiordland penguin, 60cm
      debug: "    Invalid,data" -> ["Invalid", "data"]
```

使用 cargo run --release
  
  ```bash
  cargo run --release
   Compiling greet_world_challage v0.1.0 (/Users/carl/github/rust/rust-course/packages/greet_world_challenges)
    Finished release [optimized] target(s) in 0.56s
     Running `target/release/greet_world_challage`
      Little penguin, 33cm
      Yellow-eyed penguin, 65cm
      Fiordland penguin, 60cm
  ```

