
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
queue = [1]

while queue:
    node = queue.pop(0)

    if node not in visited:
        visited.append(node)
        queue.extend(graph[node])

print("BFS:", visited)
