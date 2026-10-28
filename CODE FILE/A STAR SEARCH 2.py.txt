
graph = {
    'A': {'B': 1, 'C': 4},
    'B': {'C': 2, 'D': 3},
    'C': {'E': 5},
    'D': {'F': 2, 'G': 4},
    'E': {'G': 3},
    'F': {'G': 1},
    'G': {}
}

h = {
    'A': 5,
    'B': 6,
    'C': 4,
    'D': 3,
    'E': 3,
    'F': 1,
    'G': 0
}

open_list = ['A']
g = {'A': 0}
parent = {}

while open_list:
    current = min(open_list, key=lambda n: g[n] + h[n])
    open_list.remove(current)

    print("Selected:", current)

    if current == 'G':
        break

    for neighbor in graph[current]:
        cost = g[current] + graph[current][neighbor]

        if neighbor not in g or cost < g[neighbor]:
            g[neighbor] = cost
            parent[neighbor] = current

            if neighbor not in open_list:
                open_list.append(neighbor)

path = []
node = 'G'

while node in parent:
    path.append(node)
    node = parent[node]

path.append('A')
path.reverse()

print("Path:", " -> ".join(path))
print("Total Cost:", g['G'])
