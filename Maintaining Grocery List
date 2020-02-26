bg = float(input("Enter your budget : "))
a = {"name": [], "quantity": [], "price": []}
b = list(a.values())
na = b[0]
qu = b[1]
pr = b[2]
while True:
    try:
        ch = int(input("1.ADD\n2.EXIT\nEnter your choice : "))
    except ValueError:
        print("\nERROR: Choose only digits from the given option")
        continue
    else:
        if ch == 1 and bg>0:
            pn = input("Enter product name : ")  
            q = input("Enter quantity : ") 
            p = float(input("Enter price of the product : "))
            if p>bg:
                print("\nCAN'T BUY THE PRODUCT")  
                continue
            else:
                if pn in na:
                    ind = na.index(pn)
                    qu.remove(qu[ind])
                    pr.remove(pr[ind])
                    qu.insert(ind,q)
                    pr.insert(ind,p)
                    s = bg-sum(pr)
                    print("\namount left", s)
                else:
                    na.append(pn)
                    qu.append(q)
                    pr.append(p)
                    s = bg-sum(pr)
                    print("\namount left", s)
        elif bg<=0:
            print("\nNO BUDGET")
        else:
            break
print("\nAmount left : Rs.", s)
if s in pr:
    print("\nAmount left can buy you a", na[pr.index(s)])
print("\n\n\n GROCERY LIST is: ")
for i in range(len(na)):
    print(na[i], qu[i], pr[i])
