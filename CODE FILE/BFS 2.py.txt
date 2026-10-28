
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
queue = [1]

while queue:
    node = queue.pop(0)

    if node not in visited:
        visited.append(node)
        queue.extend(graph[node])

print("BFS:", visited)
