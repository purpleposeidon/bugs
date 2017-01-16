# Assumptions Where Bugs Hide
This is a list of mental states that prevent you from finding a bug.

Since this written in a negatory way, let's start with an example:
### True is true.
Some trickster may have gone and `#define true 0`.

I heard there was once an old compiler where `*&1 = 0` would make true false by modifying the constant table.

### The input data is correct; the following behavior is correct.
You may be convinced that the bug is someplace where it is not.

### This function is not broken.
You might be ignoring a plausible candidate.

### You are reading all of the code.
There may be a function call you didn't notice. The context may be scattered in different files. Some state might be modified by some distant code.

### There is only one thing wrong.
Plane accidents tend to be caused by multiple things going wrong at the same time.

### The thing you are debugging is the one you are editing.
Your compiler might be outputting to `a.out.v2` but you are executing `a.out.v1`, or you might be editing a backup. You may be editing function l instead of similarly shaped function I. This can be recognized by frustration growing with increasingly drastic changes, and often naturally resolves itself by the programmer trying something flagrant that should break everything but does not.

### You are actually changing the input.
### Your debugger is in the state that you think it is.
There may be a function called twice, where the first call is good, and the second call is bad, and you set a break point at the function, and are investigating the first call instead of the second.

### This function's name/argument/documentation/comments are not lies.
### The output is going someplace I could see it, but I don't, therefore there is no output.
The output may be created correctly, but whatever is displaying it has a problem. Eg a draw function may be creating vertex data, but a bad matrix is putting it somewhere the camera can't see.
### Tests are testing what you think they are testing
### The feature is actually implemented
### The repository is in an atomic change.
You may have forgotten to discard a change.
### This object/method is mutable/constant
You might be doing `constant_integer.add(23)` and ignoring the result.
### Floats are real
### An "xyz" is not "xyy" is not "xyx" is not "zyx".
This is often caused by a copy & pasting, but could also be caused by copying & pasting in an axis-indexed constant array.
### You don't need to take a break.
Coming back with fresh eyes, or someone else's, may bring clarity.
### This list is exhaustive.
????
It's probably to use this list to remind & stimulate the subconcious than to go through everything as an explicit checklist???
