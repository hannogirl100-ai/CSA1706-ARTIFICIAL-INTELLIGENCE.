
graph = {
    "V1": {"V3": 4, "V2": 9},
    "V2": {"V4": 7},
    "V3": {"V2": 2, "V4": 1},
    "V4": {"V5": 4, "V6": 8},
    "V5": {"V3": 6, "V6": 2},
    "V6": {}
}


handwritten_path = ["V1", "V3", "V4", "V5", "V6"]


print("--- Path Analysis ---")
total_weight = 0
calculation_steps = []

for i in range(len(handwritten_path) - 1):
    u = handwritten_path[i]
    v = handwritten_path[i+1]

    if u in graph and v in graph[u]:
        weight = graph[u][v]
        print(f"Edge {u} -> {v}: weight = {weight}")
        calculation_steps.append(str(weight))
        total_weight += weight
    else:
        print(f"Error: Edge {u} -> {v} does not exist in the graph.")
        break


print("-" * 25)
print(f"Formula: {' + '.join(calculation_steps)} = {total_weight}")
print(f"Total Path Weight = {total_weight} ✅")
