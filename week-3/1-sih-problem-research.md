# Today, I researched about the problem statement in SIH 2026 which is "Enabling voice communication without any network in 10 indian languages" - Problem No: SIH26173 it is posted by ISRO.

## To research we got some directions from the mentor and they are following question:

## Questions:
### 1. Why ISRO needs this solution?
- In any disaster environment where a person wants to communicate with the other person at some longer distance they cannot think, type and send a message.
- They need voice like communication solution which enables voice communication without any network.

```text
Remote/Disaster Area

Person A
   │
   │ "There is a fire near the camp!"
   ▼
  STT
   │
   │ small text data
   ▼
Low-data-rate link
   │
   ▼
  TTS
   │
   ▼
Person B
    "There is a fire near the camp!"
```


### 2. Why ISRO put it in SIH?
- The real challenge in this problem is to make it efficient for Accuracy, Model Size, RAM, CPU, 10 Languages, Offline and Low Latency. All simultaneously.
- An organization has many existing system, architectures, standards, hardware, etc where they aren't encouraged to find out different and unique solutions.


### 3. Who and when this solution is used?
- The people who wants to communicate in constrained network areas where an alert or emergency message that needs to be sent through voice.