AE = API ELEMENT
1. AE belong to NN

    for category extraction, but the relation between NNs is 'part of'. e.g. the method belong to the class.

2. AE have NN

    for category extraction, but the relation between NNs is 'part of'. e.g. The class has the method.

3. AE is like NN

    for functionality extraction, it is just like the (same as template), but 'like' in this template is a prep. e.g. Stringbuffer is like StringBuilder.

4. AE represent NN

    for category extraction, relation between NNs is 'is a'. e.g. stringbuffer represent java.lang.StringBuffer

5. AE be VBN to do

    for functionality extraction, 'VBN' cannot represent the real functionality, so filter it.  e.g. the class is designed to read file.

6. AE be VBN for doing

    for functionality extraction, 'VBN' cannot represent the functionality, so filter it. e.g. the class is used for reading file.

7. AE provide for doing

    for functionality extraction, 'provide' cannot represent the functionality, so filter it. e.g. the class provides for reading files.

8. AE be to do

    for functionality extraction, filter 'be to' and get the verb behind 'to' to extract the real functionality.  e.g. The offer_method is to just offer to the queue

9. AE be (adj) for doing

    for functionality extraction, filter 'be (adj) for' and get the verb behind 'for' to extract the real functionality. e.g. FileInputStream is for reading streams of bytes.

10. AE be RBR (than AE)

    for comparison charateristic extraction, e.g. the class is safer than another

11. AE be more/less adj (than AE)

    for comparison charateristic extraction, e.g. the class is more thread-safe than another

12. AE be VBN by NN

    for functionality extraction, e.g. the value is modified by class B.

13. AE be ADJ* NN

    for category extraction(NP1, NP2) and characteristic extractoin(ADJ), e.g. StringBuilder is a mutable sequence of characters.

14. AE be adj+

    for characteristic extraction, e.g. Instances of StringBufferare thread-safe and mutable.

15. AE be same/equivalent/... prep NN

    for functionality extraction, e.g. This class is roughly equivalent to Vector

16. AE be similar/... prep NN

	for functionality extraction, e.g. The Callable interface is similar to Runnable

17. AE be different/... prep NN

	for functionality extraction, e.g. Stringbuffer is different from StringBuilder.

18. AE MD be VBN

    for characteristic extraction, e.g. The class can be modified.

19. AE VERB adv(except only/always/properly/rather/thus/not/already/...)

    for functionality and characterstic extraction, e.g. Filereader reads file efficiently.

20. AE VERB RBR (than NN)

	for comparison functionality extraction, e.g. The class writes file faster than StringBuilder.

21. AE VERB more/less adv (than NN)

	for comparison functionality extraction, e.g. class A write files faster than class B.

22. AE allow/permit/... NN

    for characteristic extraction, e.g. This implementation permits null values and the null key.

23. AE guarantee/... NN (AE makes no guarantee ...)

	for characteristic extraction, e.g. it does not guarantee the order of the map.

24. AE prohibit/... NN

	for characteristic extraction, e.g. some implementations prohibit null elements

25. AE be adj(whose dep_ is ROOT, but it is an adj.)

    for characterstic extraction. Because the root of sentence satisfy this template is adj, it will be classified into (NN ... VBN) by mistake not (NN be adj), so we create the new template.   e.g. The methods are synchronized
