
graph = {
    1: [2, 3],
    2: [5, 6],
    3: [4, 7],
    4: [8],
    5: [],
    6: [],
    7: [8],
    8: []
}

visited = []
stack = [1]

while stack:
    node = stack.pop()

    if node not in visited:
        visited.append(node)
        stack.extend(reversed(graph[node]))

print("DFS:", visited)
