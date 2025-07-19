# gorilla
SJI Curriculum+
flowchart TD

Start([Start]) --> AskWhat[Ask what they lost]
AskWhat --> LastSeen[Ask where they last remembers seeing it]
LastSeen --> CheckBag[Check their bag]

CheckBag --> Found1{Found?}
Found1 -->|Yes| End([End])
Found1 -->|No| CheckClass[check class]

CheckClass --> Found2{Found?}
Found2 -->|Yes| End
Found2 -->|No| CheckLocker[Check their locker]

CheckLocker --> Found3{Found?}
Found3 -->|Yes| End
Found3 -->|No| AskFriend[Ask a friend]

AskFriend --> Found4{Found?}
Found4 -->|Yes| End
Found4 -->|No| KeepTrack[Keep track of attempts]

KeepTrack --> Attempt5{Attempted more than 5 times?}
Attempt5 -->|No| CheckBag
Attempt5 -->|Yes| ReportGO[Report General office]
ReportGO --> SetReminder[Set reminder to check again tomorrow]
SetReminder --> End
