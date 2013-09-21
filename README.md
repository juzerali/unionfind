Union Find [![NPM version](https://badge.fury.io/js/unionfind.png)](http://badge.fury.io/js/unionfind) 
==========

A quick union find data structure for javascript


# API

## Constructor
```
var uf = new UnionFind(size[, key])
```
Initialize the Union Find data structure with number of distinct groups to begin with. Each group will be referred to as index of the array of size `size` starting at 0. You can also provide an optional `key` function that maps these indices in a certain way. For example if you would like to refer to the groups starting with `1` provide the function `function(a){return a-1;}`. The default value is `function(a){return a;}`.

## UnionFind#union
```
uf.union(p, q);
```
Combine elements in groups p and q into a single group. In other words connect the two groups.

## UnionFind#find
```
uf.find(p);
```
Return the root (value) of the group in which `p` is.

## UnionFind#Connected
```
uf.connected(p, q);
```
Returns `true` if `p` and `p` are both in same group, false otherwise.

## UnionFind#size
```
uf.size();
```
Returns the number of elements of `uf` object.

## UnionFind#count
```
uf.count();
```
Returns the number of distinct groups left inside the object.

# Licence MIT
