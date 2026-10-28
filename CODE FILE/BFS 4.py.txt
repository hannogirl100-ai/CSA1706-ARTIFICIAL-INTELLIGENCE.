
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
queue = [0]

while queue:
    node = queue.pop(0)

    if node not in visited:
        visited.append(node)
        queue.extend(graph[node])

print("BFS:", visited)
