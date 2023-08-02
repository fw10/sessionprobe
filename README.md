![Go Version](https://img.shields.io/github/go-mod/go-version/fw10/sessionprobe)
![GitHub Downloads](https://img.shields.io/github/downloads/fw10/sessionprobe/total)

# SessionProbe 🚀⚡

`SessionProbe` is a multi-threaded pentesting tool designed to assist in evaluating user privileges in web applications. It takes a user's session cookie and checks for a list of URLs if access is possible, highlighting potential authorization issues. `SessionProbe` deduplicates URL lists and provides real-time logging and progress tracking.

`SessionProbe` is intended to be used with `Burp Suite's` "Copy URLs in this host" functionality in the `Target` tab. 

# Built-in Help 🆘

Help is built-in!

- `sessionprobe --help` - outputs the help.

# How to Use ⚙

```text
Usage:
    sessionprobe [flags]

Flags:
  -cookie  string   Session cookie to be used in the requests (required)
  -urls    string   File containing the URLs to be checked (required)
  -out     string   Output file (default: ./output.txt)
  -threads int      Number of threads (default: 10)
  -proxy   string   Use a proxy to connect to the target URL (default: "")

Examples:
    ./sessionprobe -urls ./urls.txt -threads 15 -cookie ".AspNetCore.Cookies=<cookie>" -out ./output.txt
    ./sessionprobe -urls ./urls.txt -cookie "PHPSESSID=<cookie>" -proxy http://localhost:8080
    ./sessionprobe -urls ./urls.txt -cookie "JSESSIONID=<cookie>"
```

# Setup ✅

- You can simply run this tool from source via `go run .` 
- You can build the tool yourself via `go build`

# Example Output 📋

```
Responses with Status Code: 200

https://<some-host>/<some-path>
...

Responses with Status Code: 301

...

Responses with Status Code: 302

...

Responses with Status Code: 404

...

Responses with Status Code: 502

...

```

# Features 🔎 

- <tbd>

# Bug Reports 🐞

If you find a bug, please file an Issue right here in GitHub, and I will try to resolve it in a timely manner.