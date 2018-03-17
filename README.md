# VisitedAllNodes.py
#One simple example at python with nodes 
g = {
    0:[1,2,3],
    1:[0,4],
    2:[0,4],
    3:[0,5],
    4:[5],
    5:[4,6,7],
    6:[],
    7:[]
}

def dfs_stack(g,node):                                  # dexetai dyo orismata h synarthsh to g o graphos kai 
    s = []                                              # node poy einai enas kombos
    visited = [False for k in g.keys()]                 # gemizei ton pinaka visited
                                                        #me 7 theseiw poy exoyn false arxika
                                                        # to opoio shmainei oti den exoyme episkeftei kanena kombo
    s.append(node)                                      # prosuethw sthn lista ton kombo poy kaledse h shnarthsh
    while len(s) != 0:                                  # ektypwnw th oyrs me ta stoixeia ths bgazw to prvto stoixeio
                                                        # ths poy einai to teleytaio poy mphke
        print("Stack", s)                               # epistrrefw ton pinaka visited afoy exw episkeftei oloys toyw komboyw
                                                        # exei pleon oles tiw theseis me true
        c = s.pop()
        print("Visiting", c)                            # to bazw na isoytai  se mia c metavlhth
                                                        # kanw th thesh c toy pinaka visited true poy shainei oti episkefthik    ton c node
        visited[c] = True
        for v in g[c]:
            if not visited[v]:
                s.append(v)                             
    return visited                                      
   
dfs_stack(g,0)                                          
