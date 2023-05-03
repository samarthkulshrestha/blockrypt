<div align="center">
<h1>blockrypt</h1>

samarth kulshrestha

![release version](https://img.shields.io/github/v/release/samarthkulshrestha/blockrypt?color=%23a039fa&include_prereleases&style=for-the-badge)
![code quality](https://img.shields.io/codefactor/grade/github/samarthkulshrestha/blockrypt/main?style=for-the-badge)
![top language](https://img.shields.io/github/languages/top/samarthkulshrestha/blockrypt?color=%234877f7&style=for-the-badge)
<br>
![license](https://img.shields.io/github/license/samarthkulshrestha/blockrypt?color=%23f2e85a&style=for-the-badge)
![pre-release date](https://img.shields.io/github/release-date-pre/samarthkulshrestha/blockrypt?color=%23f76ad4&style=for-the-badge)
![repo size](https://img.shields.io/github/repo-size/samarthkulshrestha/blockrypt?color=%2346d4a0&style=for-the-badge)
<br/><br/><br/>
![blockrypt logo](assets/blockrypt.png)
<br/><br>
</div>

## Introduction

<img src="assets/xkcd_blockchain.png" align="right" style="margin: 16px;" />

"The fastest way to learn how blockchains work is to build one", says
[Hackernoon](https://hackernoon.com/). **Blockrypt** is a blockchain that I
built to understand how blockchains function.

A blockchain is an immutable, sequential chain of records called Blocks.
They can contain transactions, files or any data you like, really. But the
important thing is that they’re chained together using hashes.

## Requirements

+ Make sure that [Python](https://www.python.org/) v3.6+ (along with
[pip](https://pypi.org/project/pip/)) is installed.

+ Install the required pip packages by running:

```
pip install Flask==2.3.2 requests==2.29.0
```

+ An HTTP Client (for example[Postman](https://www.postman.com/downloads/) or
[cURL](https://curl.se/)) is also needed.

## Running

+ Clone the repository.

```
git clone https://github.com/samarthkulshrestha/blockrypt.git
```

+ Enter the `blockrypt` directory.

```
cd blockrypt/
```

+ Run Blockrypt.

```
python src/blockrypt.py
```

You will be asked for a port number. Here, enter the port you want to run
Blockrypt on. The port must be idle.

## API

+ `/chain`: Returns the entire blockchain.
    + method: GET

+ `/mine`: Runs the proof of work algorithm and mines a new block on the chain.
    + method: GET

+ `/transactions/new`: Adds a transaction to a block.
    + method: POST
    + data:
    ```json
    {
        "sender": "<sender's address>",
        "recipient": "<recipient's address>",
        "amount": 7
    }
    ```

+ `/nodes/register`: Registers new nodes on the blockchain.
    + method: POST
    + data:
    ```json
    {
        "nodes": ["http://127.0.0.1:6969"]
    }
    ```
+ `/nodes/resolve`: Runs the consensus algorithm to determine the authoritative
  chain.
    + method: GET

## Contribute

 [![pull requests welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=flat-square)](https://makeapullrequest.com)
 [![python style guide](https://img.shields.io/badge/python-style%20guide-blue?style=flat-square)](https://peps.python.org/pep-0008/)

+ I <3 pull requests and bug reports!
+ Don't hesitate to [tell me my code-fu sucks](https://github.com/samarthkulshrestha/blockrypt/issues/new), but please tell me why.

## License

Blockrypt is licensed under the MIT License.
Copyright (c) 2023 Samarth Kulshrestha.
