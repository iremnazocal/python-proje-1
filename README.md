# python-proje-1

Bir listeyi düzleştiren (flatten) fonksiyon yazın. Elemanları birden çok katmanlı listelerden ([[3],2] gibi) oluşabileceği gibi, non-scalar verilerden de oluşabilir. Örnek olarak:

input: [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

output: [1,'a','cat',2,3,'dog',4,5]

i = [[1,'a',['cat'],2],[[[3]],'dog'],4,5]

temp = []
def flatten(input):
  
  if(type(input)==list):
      for i in input:
        flatten(i)
        
  else:
    temp.append(input)
  return temp
print(flatten(i))
[1, 'a', 'cat', 2, 3, 'dog', 4, 5]

2- Verilen listenin içindeki elemanları tersine döndüren bir fonksiyon yazın. Eğer listenin içindeki elemanlar da liste içeriyorsa onların elemanlarını da tersine döndürün. Örnek olarak:

input: [[1, 2], [3, 4], [5, 6, 7]]

output: [[[7, 6, 5], [4, 3], [2, 1]]

input = [[1, 2], [3, 4], [5, 6, 7],[9,10,11]]

temp = []
def reverse(arr):
  for item in arr[::-1]:
    if item==list:
      reverse(item)
    else:
      temp.append(item[::-1])
  return temp

print(reverse(input))
[[11, 10, 9], [7, 6, 5], [4, 3], [2, 1]]
