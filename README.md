# Assumptions Where Bugs Hide
This is a list of mental states that prevent you from finding a bug.

Since this written in a negatory way, let's start with an example:
### True is true.
Some trickster may have gone and `#define true 0`.

I heard there was once an old compiler where `*&1 = 0` would make true false by modifying the constant table.

### The input data is correct; the following behavior is correct.
You may be convinced that the bug is someplace where it is not.

### The component is correct.
You might be ignoring a plausible candidate.

### You are reading all of the code.
There may be a function call you didn't notice. The context may be scattered in different files. Some (global) state might be modified by some distant code.

### The program you are debugging is the one you are editing.
Your compiler might be outputting to `a.out.v2` while you are running `a.out.v1`, or you might be editing a backup. This can be recognized by frustration growing with increasingly drastic changes, and often naturally resolves itself by the programmer trying something flagrant that should break everything but does not.

### You are actually changing the input.
### Your debugger is in the state that you think it is.
There may be a function called twice, where the first call is good, and the second call is bad, and you set a break point at the function, and are investigating the first call instead of the second.

### This function's name is not lies.
### This function's documentation is not lies.
### This function is not broken.
### The output is going somewhere.
### This object is constant.
### This object is mutable. (eg, you're not doing `thing.add(whatever)` & ignoring the result.)
### The repository is in an atomic state. (There are no uncommited changes interfering with expectations.)
### An "xyz" is not "xyy" is not "xyx" is not "zyx".
This is often caused by a copy & pasting, but could also be caused by copying & pasting in a constant.
### You don't need to take a break.
### This list is exhaustive.
????
