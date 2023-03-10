Project 3 – Chord Protocol

Group Info:
Team members (Authors)
Name	          UFID        emailID
Akash Kumar	    80024442    akashkumar@ufl.edu
Ayush Kumar	    54666085    ayushkumar@ufl.edu

How its Works:
Nodes and keys are assigned to the nodes an m-bit is identified using consistent hashing and SHA-1 is used as a base in consistent hashing. It's uniformly distributed in the same identifier with significantly less collision.

Using the Chord lookup protocol, nodes and {object, keys} are arranged in an identifier circle that has at most 2^x and 0 to 2^x -1. Where x is x-bit identifier.

Each node has a successor and predecessor. The successor is the next node which is greater than the key and the processor is the previous node anti-clockwise, so for node 0, the predecessor would be 2^x-1.

What is working?
Arrays of hashed values are distributed peer-to-peer using the Chord protocol and algorithm. Different computers (known as "nodes") hold key-value pairs in distributed hash tables.

Several APIs are used to implement this protocol, including Join, successor, Stabilize, and others.This contains the code for bonus part as well.


* The chord protocol is implemented using the APIs(join, stabilize...) mentioned in the research paper. The implementation is working as expected.
After the hashing procedure specified in the specifications, x-bit reductions are carried out.
Many clashes occurred when creating distinctive node identifiers. This issue can be avoided by using random numbers.

What is the largest network you managed to deal with:
The maximum number of nodes in which our model is working is 1000 nodes with 100 messages each. The journey of a communication takes between three and five hops on average. Based on an average of 11 runs, the value was 3.91 hops. This means that the chord protocol takes 3.93 hops on average for any node to find any content. As a result, lookups take the order of log n seconds. Where n is the number of nodes in the network.

Findings:
This many nodes require substantially more time to stabilize. When there are more messages, the program performs better.


Instructions (Bonus is included):

The input provided (as command line to the program) will be of the form:

filename numNodes  numRequests

numNodes -> Required number of nodes to be set up in a chord
numRequests -> Number of messages each node sends for lookups

The input for the Bonus :

filename numNodes  numRequests numOfNodeToDelete

Output Example:
filename.erl 1000 11  
Average hops for a message: 3.198


Output Example(Bonus):

filename.erl 1000 100 12  
Average hops for a message: 3.490



