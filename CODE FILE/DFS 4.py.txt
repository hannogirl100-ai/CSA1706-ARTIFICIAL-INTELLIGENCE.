
graph = {
    0: [1],
    1: [3],
    3: [4, 2],
    4: [5],
    5: [7],
    7: [6],
    6: [4],
    2: [1]
}

visited = []
stack = [0]

while stack:
    node = stack.pop()

    if node not in visited:
        visited.append(node)
        stack.extend(reversed(graph[node]))

print("DFS:", visited)
