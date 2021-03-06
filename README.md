# dns-stamp-parser

A library to encode and decode [DNS stamp](https://dnscrypt.info/stamps-specifications).
[![Build status](https://github.com/LinkTed/dns-stamp-parser/workflows/Continuous%20Integration/badge.svg)](https://github.com/LinkTed/dns-stamp-parser/actions?query=workflow%3A%22Continuous+Integration%22)
[![Dependency status](https://deps.rs/repo/github/linkted/dns-stamp-parser/status.svg)](https://deps.rs/repo/github/linkted/dns-stamp-parser)
[![Code coverage](https://codecov.io/gh/LinkTed/dns-stamp-parser/branch/master/graph/badge.svg)](https://codecov.io/gh/LinkTed/dns-stamp-parser)
[![Latest version](https://img.shields.io/crates/v/dns-stamp-parser.svg)](https://crates.io/crates/dns-stamp-parser)
[![License](https://img.shields.io/crates/l/dns-stamp-parser.svg)](https://opensource.org/licenses/BSD-3-Clause)

## Usage

Add this to your `Cargo.toml`:

```toml
[dependencies]
dns-stamp-parser = "~3.0.0"
```

## Example

```rust
use dns_stamp_parser::DnsStamp;

fn example() {
    let stamp = "sdns://AgcAAAAAAAAADTIxNy4xNjkuMjAuMjIgPhoaD2xT8-l6SS1XCEtbmAcFnuBXqxUFh2_YP9o9uDgNZG5zLmFhLm5ldC51awovZG5zLXF1ZXJ5";
    let dns_stamp = DnsStamp::decode(stamp).unwrap();
    println!("{}", dns_stamp.encode().unwrap());
}
```
