# Assignment2

makeCacheMatrix <- function(x = matrix()) {
## set the matrix
inv <-NULL
setMatrx<-function(mat){
m<<-mat 
}
## get the matrix
getMatrix<-function() m
## set the inverse
cacheInverse<-function(temp){
inv<<-temp
}
## get the inverse
getInverse<-function(){
if (nrow(m) != ncol(m)) {print('matrix is not square')}
inv
}

list(setMatrix=setMatrix,getMatrix=getMatrix,cacheInverse=cacheInverse,getInverse=getInverse)

}

cacheSolve <- function(x) {
n<-s$getInverse()
if (!is.null(n)){
## get it from the cache and skips the computation.
message("getting cached data")
return(n)
}
## sets the value of the inverse in the cache via the setinv function.
n<-solve(s$getMatrix())
s$cacheInverse(n)
n
}
