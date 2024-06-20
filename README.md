import math

#noktaların tanımlanması:
points = [(1,2),(3,4),(5,6),(7,8)]

#öklid mesafesi için bir fonksiyon yazma:
def euclideanDistance(points1,point2):
    return math.sqrt((point2[0]-points1[0])*2 + (point2[1]-points1[1])*2)

#mesafelerin hesaplanması:
distances = []
for i in range(len(points)):
    for j in range(i+1,len(points)):
        distances.append(euclideanDistance(points[i],points[j]))

#minimum mesafenin bulunması:
min_distance = min(distances)
print("Minimum mesafe:", min_distance)
