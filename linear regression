library(pbdMPI, quietly=TRUE)
init()
table
table<-as.numeric(unlist(table))
table<-matrix(table, ncol=10)
t.X<-t(table[,-1])
A<-allreduce(t.X %*% table[,-1], op=”sum”)
B<-allreduce(t.X %*% table[,1], op=”sum”)
Beta<-solve(A,B)
Beta
