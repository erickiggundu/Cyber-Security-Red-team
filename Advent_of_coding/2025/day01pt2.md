#URL
https://adventofcode.com/2025/day/1#part2

# Instructions


You're sure that's the right password, but the door won't open. You knock, but nobody answers. You build a snowman while you think.

As you're rolling the snowballs for your snowman, you find another security document that must have fallen into the snow:

"Due to newer security protocols, please use password method 0x434C49434B until further notice."

You remember from the training seminar that "method 0x434C49434B" means you're actually supposed to count the number of times any click causes the dial to point at 0, regardless of whether it happens during a rotation or at the end of one.

Following the same rotations as in the above example, the dial points at zero a few extra times during its rotations:

    The dial starts by pointing at 50.
    The dial is rotated L68 to point at 82; during this rotation, it points at 0 once.
    The dial is rotated L30 to point at 52.
    The dial is rotated R48 to point at 0.
    The dial is rotated L5 to point at 95.
    The dial is rotated R60 to point at 55; during this rotation, it points at 0 once.
    The dial is rotated L55 to point at 0.
    The dial is rotated L1 to point at 99.
    The dial is rotated L99 to point at 0.
    The dial is rotated R14 to point at 14.
    The dial is rotated L82 to point at 32; during this rotation, it points at 0 once.

In this example, the dial points at 0 three times at the end of a rotation, plus three more times during a rotation. So, in this example, the new password would be 6.

Be careful: if the dial were pointing at 50, a single rotation like R1000 would cause the dial to point at 0 ten times before returning back to 50!

Using password method 0x434C49434B, what is the password to open the door?
# Concept
modular arathematic

# code 

ist_of_instr = [21,37,-39,-11,-3,20,7,1,49,-39,-47,27,-45,-8,-34,-48,-28,-15,22,26,40,-13,29,-38,-49,-10,12,15,15,37,30,19,-36,-42,-46,-43,-40,-49,-1,-40,-29,20,3,1>

dial_position = 50

zero_counter = 0

def dial_math(instruction):
    global dial_position
    global zero_counter
    result = (instruction + dial_position) % 100
    if result == 0:
        zero_counter += 1
    dial_position = result

for i in list_of_instr:
    if i > 0:
        for _ in range(i):
            dial_math(1)
    else:
        for _ in range(abs(i)):
            dial_math(-1)

print(f"The zero counter is : {zero_counter}")

''''


''''
