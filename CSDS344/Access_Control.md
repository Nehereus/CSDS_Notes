# Access Control
## Relationship Among Access Control and Other Security Functions
An access control mechanism mediates between a user (or a process executing on behalf of a user) and system resources, such as applications, operating systems, firewalls, routers, files, and databases. The system must first authenticate an entity seeking access. Typically, the authentication function determines whether the user permitted to access the system at all. (stalling, 141)
## protected state
- state of a system is a collection of current values of all m
  - memory locations
  - secondary storage
  - registers
  - other components of the system
- protection state is a subset of states that deal with protecting the system
- state transition is a change from one state to the next usually via a command
  - can cause change in the protection state
## type of mechanism
![](../img/2022-10-04-21-01-05.png)


## Access Control Matrix
- Access Control Matrix (ACM) is a tool to describe a protection state of the system by characterizing the rights of each subject 
- Elements of an ACM form a specification against which the current  state can be compared

### Subjects, Objects, and Access Rights
- subject: an entity who is able to access a resource
- object: a resource that can be accessed
- access right: describe how can a object be accessed by a subject

### Miscellaneous 
- class: owner, group, world
- right: read, write, execute, search, delete, create

### concept
![](../img/2022-10-04-21-18-52.png)


## an example
![](../img/2022-10-04-22-05-03.png)

## Access Controlled by History
- S set of static rights associated with procedure (i.e. each piece of “static” code)
- C set of current rights associated with each process as it executes
-  When process calls a procedure, the process rights are the interception of S and C.

### an example 
```c
function help_proc()
            return sys_kernel_file
function main()
    sys_load_file(help_proc)
    tmp_file = help_proc()
    sys_del_file(tmp_file)
```
![](../img/2022-10-04-22-18-04.png)
## state transitions
![](../IMG/2022-10-05-00-17-46.png)
- transformation procedures

## Primitive Operations
- create subject s; create object o
- destroy subject s; destroy object o
- enter r into A[s, o], delete r from A[s, o] add/remove a right
![](../IMG/2022-10-05-01-17-08.png)

### if condition
x is a right in A[s,o]
```
command foobar(p,s,o)
  if x in A[s,o]
  then
end
  
```
- bi-conditional
```
command foobar(p,s,o)
  if x in A[s,o] and y in A[s0,o]
  then
end
  
```

## Attenuation of Privilege
Principle says you cannot increase your rights or give rights you do not possess
- restrict addition of rights within a system
- often ignored for the owner, since the owner can give itself the right and then give them to others, and then delete its own right.

### copy flag and right
- copy right/grant right allows possessors to giev rights to another. 
- often attached to a right or privilege (flag), so only applies to that right. 
```
r cannot be copied
rc can be copied
```
## own right
allow the possessor to change entries in ACM column. i.e. the owner can give and delete rights to others. 
- may depends on the underlying OS