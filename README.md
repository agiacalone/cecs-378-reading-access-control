# CECS 378 Reading Assignment: Access Control

### Assignment Description
Answer the following questions from the Chapter 4 reading from your text book. Be complete with your answers. You may work on these questions with one or two other partners, but *all* students must submit the document individually in their own repositories along with each student’s name documented with the submission.

1. Briefly describe the difference between DAC and MAC.
2. List and define the four types of entities in a base model RBAC system.
3. In the NIST RBAC model, what is the difference between SSD and DSD?
4. Describe three types of role hierarchy constraints.
5. For the DAC model discussed in your textbook’s Section 4.3, an alternative representation of the protection state is a directed graph. Each subject and each object in the protection state is represented by a node (a single node is used for an entity that is both subject and object). A directed line from a subject to an object indicates an access right, and the label on the link defines the access right.
	* Draw a directed graph that corresponds to the access matrix of Figure 4.2a.
	* Draw a directed graph that corresponds to the access matrix of Figure 4.3.
	* Is there a one-to-one correspondence between the directed graph representation and the access matrix representation? Explain.
6. UNIX treats file directories in the same fashion as files; that is, both are defined by the same type of data structure, called an inode. As with files, directories include a nine-bit protection string. If care is not taken, this can create access control problems. For example, consider a file with protection mode 644 (octal) contained in a directory with protection mode 730. How might the file be compromised in this case?
7. In the traditional UNIX file access model, which we describe in your textbook’s Section 4.4, UNIX systems provide a default setting for newly created files and directories, which the owner may later change. The default is typically full access for the owner combined with one of the following: no access for group and other, read/execute access for group and none for other, or read/execute access for both group and other. Briefly discuss the advantages and disadvantages of each of these cases, including an example of a type of organization where each would be appropriate.
8. Consider user accounts on a system with a Web server configured to provide access to user Web areas. In general, this uses a standard directory name, such as `public_html`, in a user’s home directory. This acts as their user Web area if it exists. However, to allow the Web server to access the pages in this directory, it must have at least search (execute) access to the user’s home directory, read/execute access to the Web directory, and read access to any Web pages in it. Consider the interaction of this requirement with the cases you discussed for the preceding problem. What consequences does this requirement have? Note that a Web server typically executes as a special user, and in a group that is not shared with most users on the system. Are there some circumstances when running such a Web service is simply not appropriate? Explain.
9. Assume a system with N job positions. For job position i, the number of individual users in that position is Ui and the number of permissions required for the job position is Pi.
(a) For a traditional DAC scheme, how many relationships between users and permissions must be defined?
(b) For a RBAC scheme, how many relationships between users and permissions must be defined?
10. In the example of your textbook’s Section 4.8, use the notation Role(x).Position to denote the position associated with role x and Role(x).Function to denote the function associated with role x.
(a) We defined the role hierarchy for this example as one in which one role is superior to another if its position is superior and their functions are identical. Express this relationship formally.
(b) An alternative role hierarchy is one in which a role is superior to another if its function is superior, regardless of position. Express this relationship formally.
(a) The system then verifies that Pa was correctly supplied. How? (b) How can an opponent attack this system?
10. Consider the Bloom filter discussed in Section 3.3 in your textbook (Password-Based Authen- tication). Define k = number of hash functions; N = number of bits in hash table; and D = number of words in dictionary.
	* Show that the expected number of bits in the has h table that a r e equal to zero is expressed as φ = (1 − Nk )D
(b) Show that the probability that an input word, not in the dictionary, will be falsely accepted as being in the dictionary is P = (1 − φ)k
(c) Show that the preceding expression can be approximated as P ≈ (1 − e−kD/N )k