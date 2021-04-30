# a-star-search-with-heap


A* search algorithm with heap (heuristic =Euclidean distance (lat, lon))

## pseudocode:

start = node(s) 
   
destination = node(t)

D[v] = inf
   
D[s] = 0

h[v] = Euclidean distance
   
key[v] = D[v] + h[v]

pred[v] = -1

new heap

insert all the vertices into heap

while heap is not empty:
   
  popmin as u
    
  if u = t, break
    
  for all (u,v)
    
   Dv = D[u] + w(u,v)
      
   if Dv < D[v]
      
   D[v] = Dv
        
   pred[v] = u
        
   key[v] = Dv + h(v,t)
        
   Dreasekey(v,Dv)
