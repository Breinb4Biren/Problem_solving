✅ Explanation
🔁 Iterative Approach
We reverse the direction of .next pointers for each node.

Step-by-Step:
Initialize:

prev = null

current = head

While current != null:

Store next = current.next

Reverse: current.next = prev

Move prev = current, current = next

Return prev (new head)

Easy Explanation:
Reversing a linked list means changing the direction of all the next pointers.

In a normal singly linked list, each node points to the next node. For example:
1 → 2 → 3 → 4 → 5 → null
After reversing it, the pointers should flip like this:

null ← 1 ← 2 ← 3 ← 4 ← 5
Now the head becomes the tail, and the tail becomes the head.

🔁 How It Works (Step-by-Step)
To do this, we use three pointers:

Pointer	Purpose
prev:	Keeps track of the node that will come before the current node in the reversed list
current: Points to the node we're currently reversing
next:	Temporarily stores the next node so we don’t lose it during reversal

-------------

🪜 Step-by-Step Example:
Let’s say the original list is:
head → 1 → 2 → 3 → null

Initialization:
prev = null
current = head (1)

1st Iteration:
next = current.next (2)
current.next = prev (null)
prev = current (1)
current = next (2)

Now the list looks like:
1 → null   and   2 → 3 → null (to be reversed)

2nd Iteration:
next = current.next (3)
current.next = prev (1)
prev = current (2)
current = next (3)

Now:
2 → 1 → null   and   3 → null

3rd Iteration:
next = current.next (null)
current.next = prev (2)
prev = current (3)
current = next (null)

Now:
3 → 2 → 1 → null

Loop ends since current is now null. We return prev (which is the new head)

🧠 Why We Use prev and next?
Because:
Without next, we lose access to the rest of the list when we change a pointer.

Without prev, we can’t build the reversed list.

This method doesn’t need extra memory — it reuses the existing nodes.

********************

📦 Real World Applications
Undo/Redo in editors

Reversing logs, playlists

Blockchain traversal

Rollback in interpreters or systems

⏱️ Time & Space Complexity
Metric	Value
Time	O(n)
Space	O(1)