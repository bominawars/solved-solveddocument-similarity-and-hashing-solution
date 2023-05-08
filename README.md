Download Link: https://assignmentchef.com/product/solved-solveddocument-similarity-and-hashing-_solution
<br>
Overview In this assignment you will explore the use of k-grams, Jaccard distance, min hashing, and LSH in the context of document similarity. You will use four text documents for this assignment:

As usual, it is highly recommended that you use LaTeX for this assignment. If you do not, you may lose points if your assignment is difﬁcult to read or hard to follow. Find a sample form in this directory:

Creating k-Grams (40 points) You will construct several types of k-grams for all documents. All documents only have at most 27 characters: all lower case letters and space. [G1] Construct 2-grams based on characters, for all documents. [G2] Construct 3-grams based on characters, for all documents. [G3] Construct 2-grams based on words, for all documents. Remember, that you should only store each k-gram once, duplicates are ignored. A: (20 points) How many distinct k-grams are there for each document with each type of k-gram? You should report 4×3 = 12 different numbers. B: (20 points) Compute the Jaccard similarity between all pairs of documents for each type of k-gram. You should report 3×6 = 18 different numbers. 2 Min Hashing (30 points) Wewillconsiderahashfamily H sothatanyhashfunction h ∈ H mapsfrom h : {k-grams}→ [m] for m large enough (To be extra cautious, I suggest over m ≥ 10,000). A:(25points) UsinggramsG2,buildamin-hashsignaturefordocumentD1andD2usingt = {20,60,150,300,600} hashfunctions. Foreachvalueof t reporttheapproximateJaccardsimilaritybetweenthepairofdocuments D1 and D2, estimating the Jaccard similarity: ˆ JSt(a,b) = 1 t t X i=1(1 if ai = bi 0 if ai 6= bi. You should report 5 numbers. B: (5 point) What seems to be a good value for t? You may run more experiments. Justify your answer in terms of both accuracy and time. 3 LSH (30 points) Consider computing an LSH using t = 160 hash functions. We want to ﬁnd all documents which have Jaccard similarity above τ = .4. A: (8 points) Use the trick mentioned in class and the notes to estimate the best values of hash functions b within each of r bands to provide the S-curve f(s) = 1−(1−sb)r with good separation at τ. Report these values. B: (24 points) Using your choice of r and b and f(·), what is the probability of each pair of the four documents (using [G2]) for being estimated to having similarity greater that τ? Report 6 numbers. (Show your work.) 4 Bonus (3 points) Describe a scheme like Min-Hashing for the S-Dice Similarity, deﬁned S-Dice(A,B) = 2|A∩B| |A|+|B| . So given two sets A and B and family of hash functions, then Prh∈H[h(A) = h(B)] = S-Dice(A,B). Note the only randomness is in the choice of hash function h from the set H, and h ∈ H represents the process of choosing a hash function (randomly) from H. The point of this question is to design this process, and show that it has the required property. Or show that such a process cannot be done.