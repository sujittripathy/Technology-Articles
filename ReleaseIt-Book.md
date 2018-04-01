# Chapter 3 (Stabilize Your System)
  * Stopping Crack Propagation : If one part of the system fails then System it need to be designed so that other parts of the 
    System shouldn't get impacted.
  * Failure is bound to happen however, Systems need to find a way to prevent it.
# Chapter 4 (Stability Antipatterns)
 * Integration Points
   * The TCP/IP Guide [Koz05]
   * Http Protocol Timeout handling for the REST api calls
   * Beware this necessary evil. 
     * Every integration point will eventually fail in some way, and you need to be prepared for that failure.
   * Prepare for the many forms of failure.
     * Integration point failures take several forms, ranging from various network errors to semantic errors. You will not get nice error responses delivered through the defined protocol; instead, you’ll see some kind of protocol violation, slow response, or outright hang.
   * Apply patterns to avert integration point problems.
     * Defensive programming via Circuit Breaker, Timeouts (see ​Timeouts​), Decoupling Middleware, and Handshaking (see    Handshaking) will all help you avoid the dangers of integration points.
* Chain Reactions
  * Recognize that one server down jeopardizes the rest.
    * A chain reaction happens because the death of one server makes the others pick up the slack. The increased load makes them more likely to fail. A chain reaction will quickly bring an entire layer down. Other layers that depend on it must protect themselves, or they will go down in a cascading failure.
  * Hunt for resource leaks.
    * Most of the time, a chain reaction happens when your application has a memory leak. As one server runs out of memory and goes down, the other servers pick up the dead one’s burden. The increased traffic means they leak memory faster.
  * Use Autoscaling.
  * Hunt for obscure timing bugs.
* Users
  * Traffic
    * Heap Memory
    * Off-Heap Memory, Off-Host Memory (Use something like Memcached/Redis for object storage)
    * Sockets
    
    

   
