
graph = {
    1: [2, 3],
    2: [4, 5],
    3: [],
    4: [5],
    5: [2, 4]
}

visited = []
queue = [1]

while queue:
    node = queue.pop(0)

    if node not in visited:
        print(node, end=" ")
        visited.append(node)

        for neighbour in graph[node]:
            if neighbour not in visited:
                queue.append(neighbour)
