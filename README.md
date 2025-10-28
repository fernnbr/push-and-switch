```
Would it save you a lot of time if I just gave up and went mad now?
Douglas Adams, The Hitchhiker’s Guide to the Galaxy
```

---

# Welcome, Stranger (again). This is Push and Swap, but I prefer to call it Push and Switch 

We'll experience the existential crisis of sorting numbers with your hands tied behind your back. Weeeee... 

<div align="center">
<p align="center">
  <img src="https://media1.giphy.com/media/v1.Y2lkPTc5MGI3NjExN3lrMWVlYmk2Nzdrb2Z4YWZldGpmOXZ1eHFoY2lhZmdwdmI5ZXV5eiZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/jVYYMJq0ROmUursiE4/giphy.gif">
</p></figcaption>
<p align="center">
</p>
</div>

Imagine you have two stacks (let's call them a and b), a bunch of random integers, and a very specific set of operations. 
Your mission? Sort those numbers in ascending order using the minimum number of moves possible.

<div align="center">
<p align="center">
  <img src="https://media3.giphy.com/media/v1.Y2lkPTc5MGI3NjExdjJrMXVsMXozOWI3dXdqMTR0OHF0dm4wbnYxeTRtbnUybm95d2FpZyZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/l0IymiszgmwwfB5K0/giphy.gif">
</p></figcaption>
<p align="center">
</p>

That means, basically, a puzzle game where you're given a pile of shuffled numbers, two stacks, and told "sort this... but you can only swap the top two, rotate the whole stack like a Ferris wheel, or push stuff between stacks!" It's like solving a Rubik's cube where every move counts and the judges are tracking whether you can sort 500 numbers in under 5,500 moves, because apparently 5,501 moves means you're inefficient and should reconsider your life choices. 

You'll go through all five stages of grief 
denial: "this is easy!", 
anger: "WHY WON'T IT SORT?!", 
bargaining: "maybe 10,000 operations is fine?", 
depression: "I'll never optimize this", 
acceptance: "time to learn actual algorithms"

before finally emerging victorious with a beautifully optimized sorting algorithm that would make your colleagues shed a single proud tear. (or not)



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
















# 🔄 Push_swap: The Stack Sorting Challenge

> *"Because Swap_push doesn't sound as natural"*

## 🎯 What is This Madness?

Welcome to **Push_swap**, where you'll experience the existential crisis of sorting numbers with your hands tied behind your back! 

Imagine you have two stacks (let's call them `a` and `b`), a bunch of random integers, and a very specific set of operations. Your mission? Sort those numbers in ascending order using the **minimum number of moves possible**. 

Think of it as Tetris meets sorting algorithms meets "how much can we frustrate a programmer today?"

## 🎮 The Rules of Engagement

You start with:
- **Stack A**: Contains random integers (positive, negative, duplicates not allowed!)
- **Stack B**: Empty (lonely, but not for long)

Your arsenal of operations:



## 📊 The Project Stages

### Stage 1: Understanding the Beast 🤔
- Wrap your head around stack operations
- Visualize how elements move (seriously, draw it!)
- Realize this is harder than it looks

### Stage 2: The Naive Approach 🐌
- Get **something** working
- Watch in horror as it takes 10,000 operations to sort 100 numbers
- Question your life choices

### Stage 3: Algorithm Enlightenment 💡
This is where the magic happens! You'll need to:
- **Choose your fighter**: Chunk sorting? Median-based? Radix? Turk Algorithm?
- Understand time complexity (Big O notation becomes your new best friend)
- Optimize, optimize, optimize!

### Stage 4: The Benchmarks 📈

To pass with flying colors, you need:
- **100 numbers** sorted in < 700 operations (max score)
- **500 numbers** sorted in < 5,500 operations (max score)

For minimum passing:
- Various combinations between 700-1300 ops for 100 numbers
- Various combinations between 5500-11500 ops for 500 numbers

### Stage 5: The Bonus Round (Optional) 🎁
Build a **checker** program that verifies if a sequence of operations actually sorts the stack. It's like being your own teacher!

## 🔥 Why This Project Matters

### For Your Brain 🧠
- **Algorithm Design**: You'll understand WHY certain sorting algorithms exist
- **Complexity Analysis**: Learn to think in terms of efficiency, not just "does it work?"
- **Problem Decomposition**: Break down a complex problem into manageable chunks
- **Optimization Skills**: Make trade-offs between code complexity and performance

### For Your Career 💼
This project is interview prep in disguise:
- Sorting algorithms are **interview favorites**
- Time complexity discussions? Check!
- Space complexity trade-offs? Check!
- Optimizing under constraints? Check!

### For Your Soul 🎨
- The satisfaction of getting 100 numbers sorted in 500 moves
- The joy of beating your previous record
- The pride of explaining your algorithm to confused peers

## 🛠️ C Concepts You'll Master

### Memory Management 🧱
```c
// Dynamic allocation for stacks
int *stack_a = malloc(sizeof(int) * size);
// Don't forget to free! Memory leaks = instant 0
free(stack_a);
```

### Linked Lists (Probably) 🔗
Most implementations use linked lists for stack operations:
- Creating nodes
- Insertion/deletion at head
- Traversing and manipulation

### Pointer Magic ✨
```c
void swap(int **stack);
void rotate(t_stack **head);
// Pointers to pointers? Yes, please!
```

### Command-line Arguments 📝
```c
int main(int argc, char **argv)
{
    // Parse those numbers!
    // Handle errors gracefully
    // argv[1], argv[2], argv[3]...
}
```

### Error Handling 🚨
- Input validation (is it an integer? duplicate?)
- Integer overflow checks
- Memory allocation failures
- Writing to stderr vs stdout

### Makefile Mastery 🔧
```makefile
NAME = push_swap
CC = cc
CFLAGS = -Wall -Wextra -Werror

all: $(NAME)
clean: # Remove .o files
fclean: # Remove everything
re: # Recompile from scratch
bonus: # Checker program
```

## 🌍 Real-World Applications

### 1. Database Query Optimization 🗄️
Sorting data efficiently is crucial for:
- Indexing large datasets
- Optimizing JOIN operations
- Query result ordering

### 2. CPU Task Scheduling ⚙️
Operating systems use similar stack/queue operations for:
- Process scheduling
- Thread management
- Resource allocation

### 3. Data Structure Design 📚
Understanding stack operations helps with:
- Implementing undo/redo functionality
- Browser history (back/forward buttons)
- Expression evaluation (calculators)

### 4. Algorithm Interview Prep 🎤
This project covers:
- Stack-based problems (common in interviews!)
- Algorithm optimization strategies
- Complexity analysis skills

### 5. Game Development 🎮
Stack operations are used in:
- Game state management
- Pathfinding algorithms
- AI decision trees

## 🎯 Pro Tips for Success

1. **Visualize Everything**: Draw your stacks on paper before coding
2. **Start Simple**: Get 3 numbers working before tackling 500
3. **Test Religiously**: Use random number generators for testing
4. **Study Algorithms**: Look into Turk Algorithm, median-based sorting
5. **Optimize Last**: Make it work, then make it fast
6. **Peer Review**: Your classmates are your best debugging tool

## 🏆 Victory Conditions

- ✅ No memory leaks (valgrind is your friend)
- ✅ Handles all error cases gracefully
- ✅ Meets benchmark requirements
- ✅ Clean, readable code (Norminette approved)
- ✅ You can explain your algorithm without crying

## 🎪 The Bottom Line

Push_swap is deceptively simple but delightfully complex. It's not just about sorting numbers—it's about learning to think algorithmically, optimize ruthlessly, and handle constraints creatively.

Plus, you'll never look at a sorting algorithm the same way again. Every `quicksort()` you write in the future will whisper, "Remember push_swap? Remember the struggle?"

And you'll smile knowingly. Because you survived. You optimized. You conquered.

---

**Now stop reading and start sorting!** 🚀

*P.S. - If you manage to sort 500 numbers in under 4,000 operations, you're either a genius or you've discovered time travel. Either way, teach us your ways.*

