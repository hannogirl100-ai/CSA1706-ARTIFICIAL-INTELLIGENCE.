
jug1 = 0
jug2 = 0

while jug1 != 4:
    if jug1 == 0:
        jug1 = 5
        print(jug1, jug2)

    elif jug2 < 3 and jug1 > 0:
        pour = min(jug1, 3 - jug2)
        jug1 = jug1 - pour
        jug2 = jug2 + pour
        print(jug1, jug2)

    elif jug2 == 3:
        jug2 = 0
        print(jug1, jug2)

    elif jug1 == 4:
        break
