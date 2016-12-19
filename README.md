# Assumptions Where Bugs Hide
0. The input data is correct.
0. The following behavior is correct.
0. The component is correct.
0. The program you are debugging is the one you are editing.
0. You are actually changing the input.
0. There is exactly 1 input.
0. There is no input.
0. All expected inputs are being received.
0. The function does what its name implies.
0. The function does what its documentation implies.
0. "xyz" is not "xyy" is not "xzy" is not "xxx" is not "zyx".
0. The output is going somewhere.
0. The object is constant.
0. The object is not constant. (eg, you're not doing `thing.add(whatever)` & ignoring the result.)
