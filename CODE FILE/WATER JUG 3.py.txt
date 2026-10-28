
jug3 = 0
jug5 = 0
jug8 = 8

print(jug3, jug5, jug8)

# Step 1: Transfer 8L to 5L
jug5 = 5
jug8 = 3
print(jug3, jug5, jug8)

# Step 2: Transfer 5L to 3L
jug3 = 3
jug5 = 2
print(jug3, jug5, jug8)

# Step 3: Transfer 3L to 8L
jug8 = jug8 + jug3
jug3 = 0
print(jug3, jug5, jug8)

# Step 4: Transfer 5L to 3L
jug3 = 2
jug5 = 0
print(jug3, jug5, jug8)

# Step 5: Transfer 8L to 5L
jug5 = 5
jug8 = jug8 - 5
print(jug3, jug5, jug8)

# Step 6: Transfer 5L to 3L
jug5 = 4
jug3 = 3
print(jug3, jug5, jug8)

# Step 7: Transfer 3L to 8L
jug8 = jug8 + jug3
jug3 = 0
print(jug3, jug5, jug8)
