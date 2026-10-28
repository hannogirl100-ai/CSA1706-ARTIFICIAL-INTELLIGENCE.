
graph = {
    1: [2, 7],
    2: [3, 6],
    3: [4, 5],
    4: [],
    5: [],
    6: [],
    7: [8, 10],
    8: [9],
    9: [],
    10: []
}

visited = []
stack = [1]

while stack:
    node = stack.pop()

    if node not in visited:
        visited.append(node)
        stack.extend(reversed(graph[node]))

print("DFS:", visited)
