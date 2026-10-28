
graph = {
    'S': {'A': 1, 'G': 12},
    'A': {'B': 3, 'C': 1},
    'B': {'D': 3},
    'C': {'D': 1, 'G': 2},
    'D': {'G': 3},
    'G': {}
}

queue = [(0, 'S')]
visited = []
parent = {}
cost = {'S': 0}

while queue:
    queue.sort()
    current_cost, current = queue.pop(0)

    if current in visited:
        continue

    visited.append(current)
    print("Visited:", current)

    if current == 'G':
        break

    for neighbor in graph[current]:
        new_cost = current_cost + graph[current][neighbor]

        if neighbor not in cost or new_cost < cost[neighbor]:
            cost[neighbor] = new_cost
            parent[neighbor] = current
            queue.append((new_cost, neighbor))

path = []
node = 'G'

while node in parent:
    path.append(node)
    node = parent[node]

path.append('S')
path.reverse()

print("Path:", " -> ".join(path))
print("Total Cost:", cost['G'])
