# Python-
#Answer for a quiz
dic = {}
num_words = 0
with open("text.txt", 'r') as f:
    for line in f:
        l1 = line.split(" ")
        num_words += len(l1)
        for w in l1:
            dic[w] = dic.get(w, 0)+1
print("Number of words:")
print(num_words)
print('\n'.join(['%s,%s' % (k, v) for k, v in dic.items()]))
