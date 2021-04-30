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
   
&nbsp;popmin as u
    
&nbsp;if u = t, break
    
&nbsp;for all (u,v)
    
&nbsp;&nbsp;Dv = D[u] + w(u,v)
      
&nbsp;&nbsp;if Dv < D[v]
      
&nbsp;&nbsp;&nbsp;D[v] = Dv
        
&nbsp;&nbsp;&nbsp;pred[v] = u
        
&nbsp;&nbsp;&nbsp;key[v] = Dv + h(v,t)
        
&nbsp;&nbsp;&nbsp;Dreasekey(v,Dv)
