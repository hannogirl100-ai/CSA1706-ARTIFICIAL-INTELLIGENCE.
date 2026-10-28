
def minimax(tree, depth, alpha, beta, maximizing):
    if isinstance(tree, int):
        return tree

    if maximizing:
        best = -999
        for child in tree:
            value = minimax(child, depth + 1, alpha, beta, False)
            best = max(best, value)
            alpha = max(alpha, best)
            if beta <= alpha:
                break
        return best

    else:
        best = 999
        for child in tree:
            value = minimax(child, depth + 1, alpha, beta, True)
            best = min(best, value)
            beta = min(beta, best)
            if beta <= alpha:
                break
        return best


tree = [[2, 3], [5, 9], [[0, 1], [7, 5]]]

print("Optimal value:", minimax(tree, 0, -999, 999, True))
