# OOAD-WEEK11
State Diagram

```
@startuml
title  Finger Scan 
[*] -r-> Mobile : lock Mobile
Mobile : Finger Scan
Mobile -up->FingerScan : scan
FingerScan : finger print
FingerScan-r-> OpenScreen : pass/unlock
OpenScreen : appication
FingerScan-d-> Mobile : fail/again
OpenScreen -d-> [*] : buttom lock
@enduml
```
<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/scan.png">

```
@startuml
title  computer
[*] -r-> Computer : open
Computer : password
Computer-r->Login : data
Login : password
Login->Login : fail/again
Login-d->OpenScreen : pass
OpenScreen : program
OpenScreen -l->Program : use
Program-l-> [*] : close
@enduml
```
<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/com.png">

```
@startuml
title  Fan
[*] -r-> Machine: PlugIn
Machine : fan
Machine -r->Buttom : open/speed
Buttom : open/close
Buttom : speed
Buttom-d-> [*] : close/PlugOut
@enduml
```
<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/fan.png">

```
@startuml
title  ATM
[*] -r-> Machine: Insert card
Machine : ATM
Machine -up->System : password
System: password
System-r->Display  : Transaction
Display : transfer money
Display-r-> Transfermoney
Transfermoney :account number
Transfermoney :money
Transfermoney :name
Transfermoney :bank
Transfermoney-d->other:finish
other :Transaction or other
other :yes/no
other-->Display : yes
other-l-> [*] : No/Card Night
@enduml
```
<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/ATM.png">

```
@startuml
title  TV
[*] -r-> Machine: Plugin
Machine : TV
Machine -r->  Open : Buttom/Remote
Open :TV
Open-d->Display : Remote
Display : news 
Display : series
Display : orther
Display-l->Close : Buttom/Remote
Close : TV
Close-l-> [*] : closeTV
@enduml
```

<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/tv.png">

#Activity Diagram

```
@startuml
title Borrow book from library
(*) --> "People"
if "Checking member" then
  -->[member] "borrow book"
    else
  ->[No member] "Register"
  -->borrow book
  ->[End] (*)
endif
@enduml
```
<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/borrow.png">
```
@startuml
title Return book
(*) --> "member"
if "Checking period borrowed < 3 day" then
  -->[member] "Return book"
  else
  ->[Overdue/pay money] "Calculation fine"
  -->Return book
  ->[End] (*)
endif
@enduml
```
<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/return.png">
```
@startuml
title Purchase Order Online
(*) --> "Customer"
if "Checking member" then
  -->[member] "Add Shopping Cart"
    else
  ->[No member] "Register"
  -->Add Shopping Cart
  -->View Shopping Cart
  -->Pay money
  ->[End] (*)
endif
@enduml
```
<img src= "https://github.com/Siriphornyui/OOAD-WEEK11/blob/master/online.png">
