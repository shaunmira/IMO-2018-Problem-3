# IMO-2018-Problem-3
n = 6
a = []
i = 1
j = 0

while i <= n:
    a.append(i)
    j += i
    i += 1
a.append(j)

del(a[-2])

def reduce():
    a1 = [abs(a[0]-a[1]), abs(a[1]-a[2]), abs(a[2]-a[3]), abs(a[3]-a[4]), abs(a[4]-a[5])]
    for i in (a+a1):
        if (a+a1).count(i) > 1:
            print a1,
            print 'X'
            return
    a2 = [abs(a1[0]-a1[1]), abs(a1[1]-a1[2]), abs(a1[2]-a1[3]), abs(a1[3]-a1[4])]
    for i in (a+a1+a2):
        if (a+a1+a2).count(i) > 1:
            print a1, a2,
            print 'X'
            return
    a3 = [abs(a2[0]-a2[1]), abs(a2[1]-a2[2]), abs(a2[2]-a2[3])]
    for i in (a+a1+a2+a3):
        if (a+a1+a2+a3).count(i) > 1:
            print a1, a2, a3,
            print 'X'
            return
    a4 = [abs(a3[0]-a3[1]), abs(a3[1]-a3[2])]
    for i in (a+a1+a2+a3+a4):
        if (a+a1+a2+a3+a4).count(i) > 1:
            print a1, a2, a3, a4,
            print 'X'
            return
    a5 = [abs(a4[0]-a4[1])]
    for i in (a+a1+a2+a3+a4+a5):
        if (a+a1+a2+a3+a4+a5).count(i) > 1:
            print a1, a2, a3, a4, a5,
            print 'X'
            return
    print a1, a2, a3, a4, a5, 'O'              
                        
while a[n-6] < a[n-1]:
    a[n-5] = 1
    while a[n-5] < a[n-1]:
        a[n-4] = 1
        while a[n-4] < a[n-1]:
            a[n-3] = 1
            while a[n-3] < a[n-1]:
                a[n-2] = 1

                for i in a[:n-2]:
                    if a[n-2] == i:
                        a[n-2] = i+1
                     
                while a[n-2] < a[n-1]:
                    for i in a[:n-2]:
                        if a[n-2] == i:
                            a[n-2] += 1

                    if a[n-2] == a[n-1]:
                        break
                    elif a[n-2] == a[n-4]:
                        break
                    elif a[n-3] == a[n-4]:
                        break
                    elif a[n-2] == a[n-5]:
                        break
                    elif a[n-3] == a[n-5]:
                        break
                    elif a[n-4] == a[n-5]:
                        break
                    elif a[n-2] == a[n-6]:
                        break
                    elif a[n-3] == a[n-6]:
                        break
                    elif a[n-4] == a[n-6]:
                        break
                    elif a[n-5] == a[n-6]:
                        break                   

                    print a,
                    reduce()
                    a[n-2] += 1
                a[n-3] += 1
            a[n-4] += 1
        a[n-5] += 1
    a[n-6] += 1

'''first inversion'''
a[n-6] = 1
while a[n-6] < a[n-1]:
    a[n-5] = 1
    while a[n-5] < a[n-1]:
        a[n-4] = 1
        while a[n-4] < a[n-1]:
            a[n-3] = 1
            while a[n-3] < a[n-1]:
                a[n-2] = 1

                for i in a[:n-2]:
                    if a[n-2] == i:
                        a[n-2] = i+1
                     
                while a[n-2] < a[n-1]:
                    for i in a[:n-2]:
                        if a[n-2] == i:
                            a[n-2] += 1

                    if a[n-2] == a[n-1]:
                        break
                    elif a[n-2] == a[n-4]:
                        break
                    elif a[n-3] == a[n-4]:
                        break
                    elif a[n-2] == a[n-5]:
                        break
                    elif a[n-3] == a[n-5]:
                        break
                    elif a[n-4] == a[n-5]:
                        break
                    elif a[n-2] == a[n-6]:
                        break
                    elif a[n-3] == a[n-6]:
                        break
                    elif a[n-4] == a[n-6]:
                        break
                    elif a[n-5] == a[n-6]:
                        break             

                    x = a.pop()
                    a.insert(-1, x)
                    print a,
                    reduce()
                    del(a[-2])
                    a.append(x)

                    a[n-2] += 1
                a[n-3] += 1
            a[n-4] += 1
        a[n-5] += 1
    a[n-6] += 1

'''second inversion'''
a[n-6]=1
while a[n-6] < a[n-1]:
    a[n-5] = 1
    while a[n-5] < a[n-1]:
        a[n-4] = 1
        while a[n-4] < a[n-1]:
            a[n-3] = 1
            while a[n-3] < a[n-1]:
                a[n-2] = 1

                for i in a[:n-2]:
                    if a[n-2] == i:
                        a[n-2] = i+1
                     
                while a[n-2] < a[n-1]:
                    for i in a[:n-2]:
                        if a[n-2] == i:
                            a[n-2] += 1

                    if a[n-2] == a[n-1]:
                        break
                    elif a[n-2] == a[n-4]:
                        break
                    elif a[n-3] == a[n-4]:
                        break
                    elif a[n-2] == a[n-5]:
                        break
                    elif a[n-3] == a[n-5]:
                        break
                    elif a[n-4] == a[n-5]:
                        break
                    elif a[n-2] == a[n-6]:
                        break
                    elif a[n-3] == a[n-6]:
                        break
                    elif a[n-4] == a[n-6]:
                        break
                    elif a[n-5] == a[n-6]:
                        break             

                    x = a.pop()
                    a.insert(-2, x)
                    print a,
                    reduce()
                    del(a[-3])
                    a.append(x)

                    a[n-2] += 1
                a[n-3] += 1
            a[n-4] += 1
        a[n-5] += 1
    a[n-6] += 1

'''third inversion'''
a[n-6]=1
while a[n-6] < a[n-1]:
    a[n-5] = 1
    while a[n-5] < a[n-1]:
        a[n-4] = 1
        while a[n-4] < a[n-1]:
            a[n-3] = 1
            while a[n-3] < a[n-1]:
                a[n-2] = 1

                for i in a[:n-2]:
                    if a[n-2] == i:
                        a[n-2] = i+1
                     
                while a[n-2] < a[n-1]:
                    for i in a[:n-2]:
                        if a[n-2] == i:
                            a[n-2] += 1

                    if a[n-2] == a[n-1]:
                        break
                    elif a[n-2] == a[n-4]:
                        break
                    elif a[n-3] == a[n-4]:
                        break
                    elif a[n-2] == a[n-5]:
                        break
                    elif a[n-3] == a[n-5]:
                        break
                    elif a[n-4] == a[n-5]:
                        break

                    x = a.pop()
                    a.insert(-3, x)
                    print a,
                    reduce()
                    del(a[-4])
                    a.append(x)

                    a[n-2] += 1
                a[n-3] += 1
            a[n-4] += 1
        a[n-5] += 1
    a[n-6] += 1
