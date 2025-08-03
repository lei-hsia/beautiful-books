ways to implement: 

- config file
- Google Guava RateLimiter
- Algorithm: 
    - Leaky Bucket
    - Token Bucket
    - Fix Window Counter
    - Sliding Window Log:
        - fine-grained traffic control, no window boundary issue; more complex
    - Sliding Window Counter
- OOD: 
    - JobScheduler
- Distributed System: 
    - 3 hosts: 4 tokens on each hosts
    - 4q/s: 0 token left
    - 12 q: -8 tokens left, throttled for 2 seconds
    - Data consistency
    - Key: host message broadcasting
        - Mesh broadcasting: all hosts know all: O(n^2): no good
        - Gossip communication
        - Distributed Cache: e.g. Redis (in-memory store)
        - Coordination Service: ONE leader (Paxos, Raft)
        - Random leader selection
    - 

<img width="875" height="525" alt="How to integrate all this with the service" src="https://github.com/user-attachments/assets/d5bd9f2c-151c-4796-970a-e81dbb73e3f5" />
