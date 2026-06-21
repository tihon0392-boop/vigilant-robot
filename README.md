<!DOCTYPE html>
<html>
<head>
    <meta charset="UTF-8">
    <title>Мой сайт</title>
</head>
<body>
    <h1>2 задание</h1>
    <pre><code>itertools import *
def f(x,y,z,w):
    return (w==z) or (not (y<=w)) or (not x)
for a1,a2,a3,a4,a5 in product([0,1],repeat=5):
    t = [(a1,0,1,0),(a2,1,1,a3),(0,a4,a5,0)]
    if len (set(t)) == 3:
        for p in permutations ('xyzw'):
            if [f(**dict (zip(p,r))) for r in t ] == [0,0,0]:
                print(p)</code></pre>
    <h1>5 задание</h1>
    <pre><code># region 1
def n3(num):
        if num == 0:
            return '0'
        res = ''
        while num > 0:
            res = str(num % 3) + res
            num //= 3
        return res
ans = []
for i in range(1,10000):
    k3 = n3(i)
    if i % 3 == 0:
        k3 = '1' + k3 +  '02'
    else:
        k3 = k3 + str(n3(((i%3)*5)))
    result = int(k3,3)
    if result >= 177:
        ans.append(i)
print(min(ans))
# endregion
mand = []
for n in range(1,1000):
    k = bin(n)[2:]
    if k.count('1') % 2 == 0:
        k = "10" + k[2:] + "0"
    else:
        k = "11" + k[2:] + "1"
    res = int(k,2)
    if res <= 19:
        mand.append(n)
print(max(mand))</code></pre>
    <h1>8 задание</h1>
    <pre><code>from itertools import *
k = 0
for x in product(sorted('строка'), repeat=5):
    s = ''.join(x)
    k += 1
    if k % 2 == 0 and s[0] not in 'аст' and s.count('о') == 2:
        print(k,s)</code></pre>
        
</body>
</html>
