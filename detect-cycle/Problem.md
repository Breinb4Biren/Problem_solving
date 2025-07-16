🚀 Problem: Detect Cycle in Linked List

📝 Problem Statement:

Given the head of a singly linked list, determine if the linked list has a cycle in it.

A linked list has a cycle if there is some node in the list that can be reached again by continuously following the next pointer.

Return true if there is a cycle in the linked list. Otherwise, return false.

Function Signature:
public boolean hasCycle(ListNode head)

🧪 Example:

Input: head = [3,2,0,-4], tail connects to node index 1

Output: true

Explanation: There is a cycle because node -4 connects back to node 2.