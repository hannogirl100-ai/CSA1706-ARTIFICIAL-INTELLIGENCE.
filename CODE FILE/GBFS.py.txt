graph = {
    'P': ['R', 'E', 'A'],
    'R': ['E'],
    'E': ['S', 'C', 'M'],
    'A': ['M'],
    'M': ['L', 'C'],
    'L': ['Z'],
    'C': ['S', 'Z'],
    'Z': ['S'],
    'S': []
}

h = {'P':10, 'R':5, 'E':3, 'A':11, 'M':9,
     'L':9, 'C':4, 'Z':6, 'S':0}

def greedy(start, goal):
    visited = []
    queue = [start]

    while queue:
        node = min(queue, key=lambda x: h[x])
        queue.remove(node)

        if node not in visited:
            print(node, end=" ")
            visited.append(node)

            if node == goal:
                print("\nGoal reached!")
                return

            queue.extend(n for n in graph[node]
                         if n not in visited)

greedy('P', 'S')
