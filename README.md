# Distributed Hash Table - PPCA 2022

## Overview

 - A DHT can be viewed as a dictionary service distributed over a network: it provides access to a common shared key-&gt;value data store, distributed over participating nodes with great performance and scalability.
 - From a user perspective, a DHT essentially provides a map interface, with two main operations: <code>put(key, value)</code> and <code>get(key)</code>. Get will retrieve values stored at a certain key while put (often called announce) will store a value on the network. Note that many values can be stored under the same key.
 - There are many algorithms to implement DHT. For this project, you are required to <b>implement Chord protocol and Kademlia protocol</b>. You are also required to <b>implement an application of DHT</b>. Finally, you should <b>write a report for about one page</b>, probably about your architecture, innovation, features and references.
 - Some helpful documents under `\doc`
 - TA: [RainyMemory](https://github.com/Rainy-Memory)  [happypig](https://github.com/happierpig) Feel free to contact us : )

## Assignment

* Use Go to implement a Chord DHT and a Kademlia DHT with basic functions.
* Use this DHT to implement an application.
* Write a report for your whole project. 

## Syllabus

> 4 weeks is plenty of time : Please feel free to arrange your time : )

* Learn GoLang (Or learn when you need it).
* Install the development environment (Recommended : **Ubuntu**).
* Learn and implement Chord protocol.
* Learn and implement Kademlia protocol.
* Implement an application of DHT with your imagination.

## Score

GitHub repository for test: [DHT-2022](https://github.com/ACMClassCourse-2021/DHT-2022)

- 35% for the Chord Test
  - 30% + 5%: 30% for basic test and 5% for advance test.
  - Basic test: naive test without "force quit".
  - Advance test: "Force quit" will be tested. There will be some more complex tests.
- 35% for the Kademlia Test (Same as above)
- 20% for the application
- 10% for a short report and code review

## Tests

Unluckily, DHT tests cannot run successfully under Windows. So if you want to run tests by yourself, it is recommended to run tests under a **Linux virtual machine**, or employ a remote server.

If you want to debug tests by yourself, you can still use GoLand under virtual machine, or use Delve (a GoLang debugger) + GoLand if you employed a remote server.

Contact TA if you find any bug in the test program, or if you have some test ideas, or if you think the tests are too hard and you want TA to make it easier.

### Basic Test

The current test procedure is:

* There are **5 rounds** of test in total.
* In each round,
  1. **20 nodes** join the network. Then **sleep for 10 seconds.**
  2. **Put 150 key-value pairs**, **query for 120 pairs**, and then **delete 75 pairs**. There is **no sleep time between contiguous two operations**.
  3. **10 nodes** quit from the network. Then **sleep for 10 seconds**.
  4. (The same as 2.) **Put 150 key-value pairs**, **query for 120 pairs**, and then **delete 75 pairs**. There is **no sleep time between contiguous two operations**.

### Advance Test

The advance test consists of "**Force-Quit Test**" and "**Quit & Stabilize Test**".

#### Force-Quit Test

The current test procedure is:

* In the beginning, **50 nodes** join the network.
* Then **put 500 key-value pairs**.
* It follows by **9 rounds** of force quit. In each round,
  1. **5 nodes force-quit** from the network. There is **500ms of sleep time** between each force-quit operation.
  2. **Query for all key-value pairs**.

#### Quit & Stabilize Test

The current test procedure is:

* In the beginning, **50 nodes** join the network.
* Then **put 500 key-value pairs**.
* Next, **every node will quit from the network**:
  1. One node quits.
  2. After the node quitting from the network, there is **80ms of sleep time**. And then **20 key-value pairs will be queried for**.

### How to Test Your Protocol?

See [this](/doc/环境配置文档.pdf) 
