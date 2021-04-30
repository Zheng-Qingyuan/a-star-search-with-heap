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
   
&emsp;popmin as u
    
&emsp;if u = t, break
    
&emsp;for all (u,v)
    
&emsp;&emsp;Dv = D[u] + w(u,v)
      
&emsp;&emsp;if Dv < D[v]
      
&emsp;&emsp;&emsp;D[v] = Dv
        
&emsp;&emsp;&emsp;pred[v] = u
        
&emsp;&emsp;&emsp;key[v] = Dv + h(v,t)
        
&emsp;&emsp;&emsp;Dreasekey(v,Dv)
