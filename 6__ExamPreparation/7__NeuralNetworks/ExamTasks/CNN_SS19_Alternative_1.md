# CNN_SS19_Alternative_1.PNG

a) Q: Describe the backpropagation algorithm in five sentences or less

A: In neural network training the gradient of a nested function needs to be computed.
That is achieved by applying the chain rule to that nested function.
The derivative terms are from the last operation are evaluated first and so on, therefore the algorithm evaluates the gradient in reverse order compared the the forward problem.
Thus the name backpropagation.


b) Q: Convolutional neural networks apply multiple cascaded convolutions to
solve tasks. Consider a black-and-white image matrix M ∈ {0,1}p×p (i.e., feature
entries in {0,1}), a stride of s (0 < s ∈ N) and a convolutional filter matrix F of
size m ×m, where 0 < m ∈ N. Write down pseudocode to apply the filter F to
the image matrix M with a stride s. Use zero padding. Hint: Do not forget the
algorithm inputs and outputs

A:
```
ApplyConvFilter(stride s, filter F, filtersize m, image M, imagesize p)
Compute dimensions of output matrix d=(p-m)/s + 1
for i=0:d-1 do
  for j=0:d-1 do
     A[i,j] = hadamadProduct(F, M[s*i:s*i+m, s*i:s*i+m])
  end for
end for
return A
```

c) Q: Apply the convolution filter (Figure 4) to
the image matrix (Figure 3). Your answer must be a matrix

A:

18 | 24 | 8
-|-|-
18 | 23 | 6 
25 | 22 | 12 
