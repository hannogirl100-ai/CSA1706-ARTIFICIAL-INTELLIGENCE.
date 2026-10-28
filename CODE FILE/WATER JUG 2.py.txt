
jug12 = 12
jug8 = 0
jug5 = 0

print(jug12, jug8, jug5)

# Step 1: Transfer from 12L to 8L
jug8 = 8
jug12 = jug12 - 8
print(jug12, jug8, jug5)

# Step 2: Transfer from 8L to 5L
jug5 = 5
jug8 = jug8 - 5
print(jug12, jug8, jug5)

# Step 3: Empty the 5L jug into the 12L jug
jug12 = jug12 + jug5
jug5 = 0
print(jug12, jug8, jug5)

# Step 4: Transfer from 8L to 5L
jug5 = jug8
jug8 = 0
print(jug12, jug8, jug5)

# Step 5: Fill the 8L jug from the 12L jug
jug8 = 8
jug12 = jug12 - 8
print(jug12, jug8, jug5)

# Step 6: Transfer from 8L to 5L until full
pour = 5 - jug5
jug5 = jug5 + pour
jug8 = jug8 - pour
print(jug12, jug8, jug5)

# Step 7: Empty the 5L jug into the 12L jug
jug12 = jug12 + jug5
jug5 = 0
print(jug12, jug8, jug5)
