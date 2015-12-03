# ComputeFramework

**A framework for DAG-based computations**

The goal is to allow a sufficient scope for dispatch at various levels of:

- Computation and recomputation
- Partitioning, rearranging data
- Caching and saving


**AbstractNode**

An abstract type for a node in the computation DAG

**DataNode <: AbstractNode**

A node that does not require further computation. For example, a BlocksNode or HDFSNode, or DistMemory

**ComputeNodes <: AbstractNode**

Nodes that represent computation. When `compute` is called on a `ComputeNode` it results in a `DataNode`.
