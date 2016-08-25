# Getting Started with Torch7

 The package 'torch' is the primary package for Torch7. it contains multi-dimensional tensor data structures and mathematical operation
 as well as a bunch of other really useful utilities such as File IO.


```lua
require 'torch'
```



 Tensor provides all of the tensor objects for numerical arrays with n-dimensionality with type templating.
 Whilst most numeric operations are only implimented for FloatTensor and DoubleTensor, other tensor types are
 useful in situations where memory space is at a premium. There are several primitive types of Tensors.

```lua
 IntTensor
 LongTensor
 FloatTensor
 DoubleTensor
 ByteTensor
 CharTensor
 ShortTensor
```

 A tensor is nothing more than an n-dimensional matrix, the number of dimensions for a tensor is essentially unlimited.
```lua
 -- we can create a 4D 2x3x3x2 tensor
 tensorA = torch.Tensor(2, 3, 3, 2)
 --- Dimensions of a Tensor can queried with nDimension() or dim()
 print(tensorA:nDimension(), tensorA:dim())
```
 Te internal data representation of a Tensor is contained within a Storage.

```lua
 IntStorage
 LongStorage
 FloatStorage
 DoubleStorage
 ByteStorage
 CharStorage
 ShortStorage
```

A LongStorage can be used to specify dimensionality.
```lua
storage = torch.LongStorage(6)
--- Dimensionality of the LongStorage can be assigned as follows, in this case we would like to create a 4x4x4x4x4x4 tensor.
storage[1] = 4; storage[2] = 4; storage[3] = 4; storage[4] = 4; storage[5] = 4; storage[6] = 4;
tensorB = torch.Tensor(storage)
```

 The internal data representation can be retrieved with storage().

```lua
tensorC = torch.Tensor(2, 10)
store = tensorC:storage()
for i=1, #store do -- Fill the Storage
    store[i] = i * 2
end

print(store)
print(tensorC)
```

It is important to note that all functions within the Tensor class manipulate the existing tensor, or
return a new tensor which is referencing the same storage.

```lua
tensorX = torch.Tensor(5):zero() --- Initialise a new Tensor filled with zeros.
print(tensorX)
tensorX:fill(1)
print("Filled with 1s:")
print(tensorX)
print(tensorX:narrow(1, 2, 3):fill(2)) --- narrow(dim, index, size) Returns a new Tensor which is a narrowed version of the current
print("Narrow returns a new tensor, but it shares the same underlying storage")
print(tensorX)
```

 If you require a copy of the Tensor, you must use the clone() method which is a helper function for torch.Tensor(x:size()):copy(x)
```lua
 tensorY = tensorX:clone()
 print(tensorY)
```

Torch also provides functions for manipulating Tensor objects. The torch packages adopts an object oriented syntax,
however all functions also support passing the target Tensor(s) as the first arguement(s)
```lua
print( torch.sum(tensorC) )
--- Is equivilent to
print( tensorC:sum())

print(torch.sqrt(36))
print(tensorX * 3 - tensorY)
print(tensorX:pow(2))

```

## Exercise

Add two tensors

```lua
function addTensors(a,b)
    return a -- FIX ME
end

a = torch.ones(5,2)
b = torch.Tensor(2,5):fill(4)
print(addTensors(a,b))
```

 Using torch functions, calculate the [euclidean distance](https://en.wikipedia.org/wiki/Euclidean_distance) of A -> B (you should get ~5.83095)

```lua
A = torch.Tensor({2, -1, 2})
B = torch.Tensor({-2, 2, -1})

function euclideanDistance(a, b)
    local distance = 0 --- Change this
    return distance
end

print(euclideanDistance(A, B))
```
