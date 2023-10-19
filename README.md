# GFG-potd 19/10/2023

 queue<int> q;
	    vector<int> vis(V,0);
	    int level= 0 ;
	    q.push(0);
	    vis[0]=1;
	    while(!q.empty()){
	        int size = q.size();
	        int i;
	          for(i = 0;i<size;i++){
	              int adjnode = q.front();
	              q.pop();
	               
	              if(adjnode == X){
	                  return level;
	              }
	              for(auto x: adj[adjnode]){
	                  if (!vis[x]){
	                      vis[x]=1;
	                      q.push(x);
	                  }
	              }
	          }
	          level++;
	    }
	    return -1;
