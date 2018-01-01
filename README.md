# Generic-Unity-Object-Pooler
An easy to use object-pooler which is efficient and fast.

# What is pooling? 
It is computationally expensive to instantiate and destroy objects like bullets that get re-used a lot.
Its a lot more effective to instantiate them all in the beginning and to keep re-using them by setting them active/false

This script can act as a pooling control hub, it will create all pooled objects you need at the start and objects can be called as and when needed by other scripts.

# How to use?
1) Create a new empty GameObject.
2) Create a new script called ObjectPooler
3) Replace the contents of ObjectPooler with contents of the ObjectPooler script that can be found in this repo.
4) Attach the script to the GameObject you created.
5) In the inspector, in the script component, enter the number of gameObjects you want pooled and then add their prefabs to the list.
6) Get the gameObject by using 

GameObject GO = ObjectPooler.SharedInstance.GetPooledObject(0);
(Instead of instantiating a new one.)

7) Make sure that the gameObject you are re-using does infact get disabled naturally after a while.
(Otherwise there is no point of pooling)

If you still have doubts, you can try running the sample scene included in the package. Simply Import a custom package, select the package and navigate to a scene where you can press the spacebar to get lots of object-pooled balls that disable after 5 seconds.

