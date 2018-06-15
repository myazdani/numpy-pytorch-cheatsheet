# NumPy to PyTorch Cheatsheet

Just my scrappy cheat sheet for looking up things in pytorch that I know in numpy - until I find a better cheatsheet. 

Even though there are a lot of similarities in syntax between the two, occasionally something is different that throws me off. 

## Array creation

Numpy                 | PyTorch                | Notes
----------------------|------------------------|----------
`np.empty((2, 2))`    | `torch.empty(5, 3)`    | empty array
`np.random.rand(3,2)` | `torch.rand(5, 3)`     | random 
`np.zeros((5,3))`     | `torch.zeros(5, 3)`    | zeros
`np.array([5.3, 3])`  |`torch.tensor([5.3, 3])`| from list
`np.random.randn(*a.shape)`|`torch.randn_like(a)`| 
`np.arange(16)`       | `torch.range(0,15)` | array starting <br>from 0 ending at <br>15 (inclusive)


## Math operations

Numpy                 | PyTorch                | Notes
----------------------|------------------------|----------
`x+y`                 | `x+y` <br> `y.add_(x)` <br> `torch.add(x,y)`| addition
`np.dot(x,y)` <br> `np.matmul(x,y)`| `torch.mm(x,y)` <br> `x.mm(y)` | matrix multiplication
`x*y`                 | `x*y`                  | element-wise multiplication
`np.max(x)`           | `torch.max(x)`         | 
`np.argmax(x)`        | `torch.argmax(x)`      |
`x**2` | `x**2` | Element-wise powers

## Array manipulations

Numpy                 | PyTorch                | Notes
----------------------|------------------------|----------
`x.T` <br> `np.transpose(x)`| `torch.transpose(x, 0, 1)` <br> `torch.transpose(x, 1, 0)`     | transpose
`a = a.reshape(-1, 2)` | `a = a.view(-1,2)` | reshape array to <br> have two columns and <br> however as many rows
`np.concatenate([a, b])` | `torch.cat([a,b])` | concatenate list of <br> arrays/tensors

A lot more summarized here but need to re-organize: https://jhui.github.io/2018/02/09/PyTorch-Basic-operations/