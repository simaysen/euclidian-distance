# euclidian-distance
IBM ile Kodluyoruz 11. Atölye ödevi

import math
points = [(1, 2), (3, 8), (6, 9)]
distances = []

"""defining the basic formula of euclid distance calculation"""
def euclidianDistance(p1, p2):
  return math.sqrt((p1[0] - p2[0])**2 + (p1[1] - p2[1])**2)


"""making sure that we don't compare the same points"""
for i in range(len(points)): 
  for j in range(i + 1, len(points)):
    dist = euclidianDistance(points[i], points[j])
    distances.append(dist)


min_distance = min(distances)

print(f"Minimum Öklid mesafesi: {min_distance: .2f}")
