```
Would it save you a lot of time if I just gave up and went mad now?
Douglas Adams, The Hitchhiker’s Guide to the Galaxy
```

---

# Welcome, Stranger (again). 
# This is Push and Swap, but I prefer to call it Push and Switch 

_We'll experience the existential crisis of sorting numbers with your hands tied behind your back. Weeeee..._ 


<p align="center">
  <img src="https://media4.giphy.com/media/v1.Y2lkPTc5MGI3NjExYmFobHB6MG95emE2bGc1bnV0c3VuMGFndjdwM2xlYzk3ZHMyamtmaSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/7LE0z2EEAiVCU/giphy.gif">
</p></figcaption>
<p align="center">
</p>
</div>


### Imagine you have two stacks (let's call them a and b), a bunch of random integers, and a very specific set of operations. Your mission? Sort those numbers in ascending order using the minimum number of moves possible.



<p align="center">
  <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExdjJrMXVsMXozOWI3dXdqMTR0OHF0dm4wbnYxeTRtbnUybm95d2FpZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l0IymiszgmwwfB5K0/giphy.gif">
</p></figcaption>
<p align="center">
</p>

That means, basically, a puzzle game where you're given a pile of shuffled numbers, two stacks, and told "sort this... but you can only swap the top two, rotate the whole stack like a Ferris wheel, or push stuff between stacks!" It's like solving a Rubik's cube where every move counts and the judges are tracking whether you can sort 500 numbers in under 5,500 moves, because apparently 5,501 moves means you're inefficient and should reconsider your life choices. 

You'll go through all five stages of grief 

1. **Denial:** "this is easy!", 
2. **Anger:** "WHY WON'T IT SORT?!", 
3. **Bargaining:** "maybe 10,000 operations is fine?", 
4. **Depression:** "I'll never optimize this", 
5. **Acceptance:** "time to learn actual algorithms"

... before finally emerging victorious with a beautifully optimized sorting algorithm that would make your colleagues shed a single proud tear. _(or not)_

---

# Let's get serious now 

This is an **algorithmic optimization project implemented in C** that requires **sorting a random sequence of unique integers using two stacks (A and B)** and a constrained set of **eleven operations**: 

1. **swap** (sa, sb, ss),
2. **push** (pa, pb),
3. **rotate** (ra, rb, rr), and
4. **reverse rotate** (rra, rrb, rrr).

The **primary objective is to develop an efficient sorting algorithm that minimizes the number of operations required to sort the input**, with performance benchmarks set at:
<700 operations for 100 elements and <5,500 operations for 500 elements to achieve maximum validation. 

The project emphasizes understanding **algorithmic complexity** (time and space), implementing **dynamic data structures** (typically linked lists for stack representation), **managing memory allocation/deallocation**, **parsing command-line arguments with robust error handling**, and **applying sorting algorithm concepts** such as: 

- chunk-based partitioning,
- median-finding, or
- radix-like approaches

Adapted to the stack constraint model. All while adhering to strict coding standards and demonstrating proficiency in low-level C programming concepts including pointer manipulation and modular program design.


<p align="center">
  <img src="https://media2.giphy.com/media/v1.Y2lkPTc5MGI3NjExamJ4MG0wOHg1ZjZ5NnEzeHRqY3liMnRhbmx0dHAxamFoemxkYTBsOSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/0hJuljU5QiB0S3j2Au/giphy.gif">
</p></figcaption>
<p align="center">
</p>
</div>


--- 

# The Rules of Engagement
We'll start with:

- Stack A: Contains random integers (positive, negative, duplicates not allowed!)
- Stack B: Empty (lonely, but not for long)

# Operations 

| Operation | What It Does | Think of It As... |
|-----------|--------------|-------------------|
| `sa` / `sb` | Swap top 2 elements | "Oops, wrong order!" |
| `pa` / `pb` | Push from one stack to another | "Get over here!" |
| `ra` / `rb` | Rotate up (first becomes last) | Ferris wheel going up ↑ |
| `rra` / `rrb` | Reverse rotate (last becomes first) | Ferris wheel going down ↓ |
| `ss` / `rr` / `rrr` | Do both stacks simultaneously | Efficiency! |


# Why This Project Matters

### For Our Brain 

- Algorithm Design: We'll understand WHY certain sorting algorithms exist
- Complexity Analysis: We'll learn to think in terms of efficiency, not just "does it work?"
- Problem Decomposition: We'll break down a complex problem into manageable chunks
- Optimization Skills: We'll make trade-offs between code complexity and performance

### For Our Career 

- Learn sorting algorithms (the interview favorites)
- Time complexity discussions?
- Space complexity trade-offs?
- Optimizing under constraints?

### For Our Soul 

- Learn resilience 
- Reach the satisfaction of getting 100 numbers sorted in 500 moves (weeeee) 
- The joy of beating your previous record (or not) 
- The pride of explaining your algorithm to confused peers (that's fun)

# Real-world use 
  
### Database Query Optimization 
Sorting data efficiently is crucial for:

- Indexing large datasets
- Optimizing JOIN operations
- Query result ordering

### CPU Task Scheduling 
Operating systems use similar stack/queue operations for:

- Process scheduling
- Thread management
- Resource allocation

### Data Structure Design 
Understanding stack operations helps with:

- Implementing undo/redo functionality
- Browser history (back/forward buttons)
- Expression evaluation (calculators)

### Algorithm Interview Prep
This project covers:

- Stack-based problems (common in interviews!)
- Algorithm optimization strategies
- Complexity analysis skills

### Game Development
Stack operations are used in:

- Game state management
- Pathfinding algorithms
- AI decision trees


---

# Victory Conditions


<p align="center">
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExNHNkY2UzazdxanB6YXR0Zzh4eXozbWowemhuNG5oZDVnMndmaXo5aSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/uTuLngvL9p0Xe/giphy.gif">
</p></figcaption>
<p align="center">
</p>
</div>


✅ No memory leaks (valgrind is your friend)

✅ Handles all error cases gracefully

✅ Meets benchmark requirements

✅ Clean, readable code (Norm approved)

✅ You can explain your algorithm without crying _(hard task)_


---

# To Know More 

### Linked Lists: Your Stack's Backbone

Think of a linked list as a conga line at a party. Each person (node) holds hands with the person behind them, but they have no idea who's at the back of the line. Want to add someone? They jump in at the front! Want to remove someone? Snip the connection! Want to find the 50th person? Well... you gotta walk through all 49 people in front of them. It's efficient for some things, painfully slow for others—just like that friend who insists on "optimizing" the group's restaurant choice. 

#### Why Linked Lists for Push_swap?

**Dynamic Size:** You don't know how many numbers you'll get. Arrays require fixed size; linked lists grow and shrink beautifully.
Efficient Stack Operations:

- push = O(1) - Just add to the head
- pop = O(1) - Just remove from the head
- rotate = O(1) - Move head to tail (with tail pointer)

### Error Handling: The Art of Saying "Nope"

Error handling is like being a bouncer at an exclusive club. 
"Not a number? NOPE.", 
"Duplicate entry? NOPE.",
"Integer overflow? NOPE.",
"Empty argument? NOPE." 

Your program needs to be that friend who politely but firmly tells people when they're being ridiculous, 
except instead of saying "maybe you've had enough," you print Error\n to stderr and exit like a boss.

# Memory Management: Don't Leak Like a Sieve


<p align="center">
  <img src="https://media0.giphy.com/media/v1.Y2lkPTc5MGI3NjExaXljMWI4aDZ2MDU4dmRrbmp0aHl3bWttaGhrdnY0dXpxaGZlamxvcCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/BBkKEBJkmFbTG/giphy.gif">
</p></figcaption>
<p align="center">
</p>
</div>


Memory management is like borrowing your friend's car. 
You malloc (borrow it), you use it, and then you absolutely must free it (return it) when you're done. 

Forget to free? 
That's a memory leak—like borrowing cars and never returning them until you have 500 cars in your driveway and no one will lend you anything anymore. 
Valgrind is that friend who keeps receipts and will 100% call you out on every unreturned car.

# Now stop reading and start sorting! 






