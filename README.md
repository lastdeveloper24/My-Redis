Redis Project:

Redis is a in memory data structure store,used as a distributed, in-memory key-value database. The name Redis means REmote Dictionary Server.There is one Redis Project 
which is sponsered by Redis Labs.
My project is not replica of that , but it is inspired from The Redis open source project backed by Redis Labs.


Redis provides access to mutable data structures via a set of commands, which are sent using a server-client model with TCP sockets and a simple protocol. 
So different processes can query and modify the same data structures in a shared way.

-----------------------------------------------------------------------------------------------------------------------------------------------------------------
RUN:

Run the server by ./server PORT(give the port number here)

-------------------------------------------------------------------------------------------------------------------------------------------------------------------
Connect The Client:

After starting the server, in a seperate terminal do the following:
./client PORT(give the port number here)

Till now I've implemented only two commands: 1.SET 2.GET

----------------------------------------------------------------------------------------------------------------------------------------
1.SET Command:

Set key to hold the string value. Both the key and value are of string type. If any key is already present its value is overwritten. 
Time complexity: O(1). 
Return value: 1. 
Syntax: SET [KEY] [VALUE] 
e.g:   

    redis> set Fizz Buzz // Fizz is the key and Buzz is the value
    redis> 1.
  
Data Structure Used: Unordered_map

unordered_map is an associated container that stores elements formed by combination of key value and a mapped value.It is found in C++ STL(Standard Template Library). 
Internally unordered_map is implemented using Hash Table, the key provided to map are hashed into indices of hash table that is why performance of data structure depends on 
hash function a lot but on an average the cost of search, insert and delete from hash table is O(1).

-------------------------------------------------------------------------------------------------------------------------------------------

2.GET Command:

GET command returns the value of the key. If the key is not present in the data base then NIL is returned.
Time Complexity: O(1)
Syntax: GET [key]
e.g:

      redis> set Fizz Buzz
      redis> 1
      redis> get Fizz
      redis> Buzz
      redis> get Head 
      redis> nil    //because head is not present in the database

Data structure Used: unordered_map


N.B:- I'm currently working on this project to implement more Commands and Functionalities. For any suggestion feel free to drop message into upstartpssi@gmail.com
