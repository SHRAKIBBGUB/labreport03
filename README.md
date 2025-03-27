# labreport03









def is_safe(graph, color_assignment, vertex, color):
    for neighbor in graph[vertex]:
        if color_assignment[neighbor] == color:
            return False
    return True

def graph_coloring_util(graph, k, color_assignment, vertex):
    if vertex == len(color_assignment):
        return True
    
    for color in range(1, k + 1):
        if is_safe(graph, color_assignment, vertex, color):
            color_assignment[vertex] = color
            if graph_coloring_util(graph, k, color_assignment, vertex + 1):
                return True
            color_assignment[vertex] = 0
    return False

def main():
    print("Graph Coloring Problem")
    
    
    N = int(input("Enter number of vertices: "))
    M = int(input("Enter number of edges: "))
    K = int(input("Enter number of colors: "))
    
   
    graph = [[] for _ in range(N)]
    print("Enter edges (vertex pairs, 0-based):")
    for _ in range(M):
        u, v = map(int, input().split())
        graph[u].append(v)
        graph[v].append(u)
    
   
    color_assignment = [0] * N
    if graph_coloring_util(graph, K, color_assignment, 0):
        print(f"\nColoring Possible with {K} Colors")
        print("Color Assignment:", color_assignment)
    else:
        print(f"\nColoring Not Possible with {K} Colors")

if __name__ == "__main__":
    main()
