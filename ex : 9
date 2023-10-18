import itertools
import math

def euclidean_distance(point1, point2):
    return int(math.sqrt((point1[0] - point2[0])**2 + (point1[1] - point2[1])**2))

def total_distance(path, cities):
    return sum(euclidean_distance(cities[path[i]], cities[path[i+1]]) for i in range(len(path)-1))

def traveling_salesman(cities):
    n = len(cities)
    min_distance = float('inf')
    best_path = None
    for path in itertools.permutations(range(n)):
        distance = total_distance(path, cities)
        if distance < min_distance:
            min_distance = distance
            best_path = path
    return best_path, min_distance

if __name__ == "__main__":
    cities = [(0, 0), (1, 4), (3, 2), (3, 1)]
    best_path, min_distance = traveling_salesman(cities)
    print(cities)
    print(f"The best path is {best_path} with a total distance of {min_distance}")
