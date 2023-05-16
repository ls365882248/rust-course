# Rust Course

这里不做环境配置的总结，详细和查看[官方文档](https://course.rs/into-rust.html)。

> 1-x 小试牛刀， 2-x 基础入门，3-x 入门实践，4-x 高级进阶

## 基础
常见命令

### 创建项目
```bash
cargo new hello_world
cd hello_world
```

### 启动项目
```bash
cargo run
```

> 可以通过 cargo run --release 来启动项目，这样会启动一个优化过的版本，但是编译时间会比较长。


### 编译项目
```bash
cargo build
./target/debug/hello_world
```

> 可以通过 cargo build --release 来编译项目，这样会启动一个优化过的版本，但是编译时间会比较长。

### 检查项目
```bash
cargo check
```

```
$ cargo check
    Checking world_hello v0.1.0 (/Users/carl/github/rust/rust-course/packages/world_hello)
    Finished dev [unoptimized + debuginfo] target(s) in 0.24s
```

### Cargo.toml 和 Cargo.lock

Cargo.toml 是 cargo 特有的项目数据描述文件。它存储了项目的所有元配置信息，如果 Rust 开发者希望 Rust 项目能够按照期望的方式进行构建、测试和运行，那么，必须按照合理的方式构建 Cargo.toml。

Cargo.lock 文件是 cargo 工具根据同一项目的 toml 文件生成的项目依赖详细清单，因此我们一般不用修改它，只需要对着 Cargo.toml 文件撸就行了。

### package 配置段落和自定义项目依赖

```toml
[dependencies]
rand = "0.3"
hammer = { version = "0.5.0"}
color = { git = "https://github.com/bjz/color-rs" }
geometry = { path = "crates/geometry" }
```

## FAQ

### 安装 Rust 环境

> https://course.rs/first-try/installation.html

### 依赖下载慢

> https://course.rs/first-try/slowly-downloading.html