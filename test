#Retrives the text files and user input
numb = int(input("Please enter a number: "))
common = open("common.txt")
text = open("alice_in_wonderland.txt")

c = common.read()
t = text.read()

#Splits the files into lists of words
comm = c.split("\n")
alice = t.replace("\n", " ")
alice = alice.lower()
alice = alice.split(" ")

#Neaten the alice list
for i in range(len(alice)):
	alice[i] = alice[i].strip("")
	alice[i] = alice[i].strip(",`';-:!?.()")
#end for
while "" in alice:
	alice.remove("")
#end while

#Removes the list of common words from the text
for i in comm:
	while i in alice:
		alice.remove(i)
	#end if
#End if

#Dictionary with the number of times a word is in the lsit
words = {}
for i in alice:
	if i not in words:
		words[i] = alice.count(i)
#End if

#Sort the dictionary
list = dict(sorted(words.items(), key=lambda x: x[1], reverse=True))
#print(list)


#Output
#print(text.read())
count = 0
print("Count Word")
print("=== ==== ")
output = "{} {}"
for i in list:
	print(output.format(words.get(i), i))
	count = count + 1
	if count >= numb:
		break
#End for

#Close the text files
common.close()
text.close()

#end
