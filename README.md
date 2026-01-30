# Inheritance and Delegation

The handout for Lab 3 can be found at: [https://github.com/CMU-17-214/s2026/blob/main/labs/lab03.md](https://github.com/CMU-17-214/s2026/blob/main/labs/lab03.md)

# Task 3
1. Which is more dependent on the implementation details of the SortedIntList, delegation or inheritance? 
- Inheritance

2. If the add method in SortedIntList is significantly modified or its behavior changes, which implementation is more likely to break?
- Inheritance
3. What issues does using delegation solve that might have been problematic with inheritance?
- Delegation reduces coupling. With inheritance, when SortedIntList changes internally, the subclass automatically inherits those changes, which may break it. With delegation, the internal implementation of SortedIntList does not affect DelegationSortedIntList as long as the interface stays the same. This makes the code more stable and easier to maintain.

4. Based on the provided implementations, when would it be more appropriate to use inheritance and when to use delegation?
- Use inheritance for IS-A relationships. The subclass truly is a special type of the parent class. Use delegation for HAS-A relationships. The class contains another object and wants to add behavior around it, not replace the parent. Inheritance ties classes tightly together, making changes risky. Delegation is more flexible because the delegated object can be replaced or changed without affecting the main class. 