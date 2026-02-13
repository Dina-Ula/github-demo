# Accounting Settlement Assignment Scenarios

## Rule Definitions

-   Rule 1: Payment accounting settlement date and cycle is greater than
    or equal to the current accounting settlement date and cycle.
-   Rule 2: Payment accounting settlement date and cycle is greater than
    the latest USM 979 Complete accounting settlement date and cycle.
-   Rule 3: Payment accounting settlement date and cycle is less than or
    equal to the latest USM 979 Complete accounting settlement date and
    cycle.

------------------------------------------------------------------------

## Settlement Cycle 1 to Settlement Cycle 2 Boundary (Monday to Thursday)

  ------------------------------------------------------------------------------------------------------
  Scenario      Payment      Derived        Current      Latest USM 979 Assigned     Rule      Outcome
  description   scheme       accounting     accounting   Complete       accounting   Applied   
                settlement   settlement     settlement   accounting     settlement             
                date and     date and cycle date and     settlement     date and               
                cycle        (from payment) cycle        date and cycle cycle                  
  ------------- ------------ -------------- ------------ -------------- ------------ --------- ---------
  Payment       Monday 02    Monday 02      Monday 02    Friday 30      Monday 02    Rule 1    Correct
  arrives       February     February 2026, February     January 2026,  February               
  during        2026, cycle  cycle 1        2026, cycle  cycle 3        2026, cycle            
  settlement    1                           1                           1                      
  cycle 1                                                                                      

  Payment       Monday 02    Monday 02      Monday 02    Friday 30      Monday 02    Rule 2    Correct
  arrives       February     February 2026, February     January 2026,  February               
  immediately   2026, cycle  cycle 1        2026, cycle  cycle 3        2026, cycle            
  after         1                           2                           1                      
  settlement                                                                                   
  cycle 2                                                                                      
  begins but                                                                                   
  USM Complete                                                                                 
  not yet                                                                                      
  received                                                                                     

  Payment       Monday 02    Monday 02      Monday 02    Monday 02      Monday 02    Rule 3    Correct
  arrives after February     February 2026, February     February 2026, February               
  USM Complete  2026, cycle  cycle 1        2026, cycle  cycle 1        2026, cycle            
  for cycle 1   1                           2                           2                      
  has been                                                                                     
  received                                                                                     
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## Settlement Cycle 2 to Settlement Cycle 3 Boundary (Monday to Thursday)

  ------------------------------------------------------------------------------------------------------
  Scenario      Payment      Derived        Current      Latest USM 979 Assigned     Rule      Outcome
  description   scheme       accounting     accounting   Complete       accounting   Applied   
                settlement   settlement     settlement   accounting     settlement             
                date and     date and cycle date and     settlement     date and               
                cycle        (from payment) cycle        date and cycle cycle                  
  ------------- ------------ -------------- ------------ -------------- ------------ --------- ---------
  Payment       Tuesday 03   Tuesday 03     Tuesday 03   Tuesday 03     Tuesday 03   Rule 1    Correct
  arrives       February     February 2026, February     February 2026, February               
  during        2026, cycle  cycle 2        2026, cycle  cycle 1        2026, cycle            
  settlement    2                           2                           2                      
  cycle 2                                                                                      

  Payment       Tuesday 03   Tuesday 03     Wednesday 04 Tuesday 03     Tuesday 03   Rule 2    Correct
  arrives       February     February 2026, February     February 2026, February               
  immediately   2026, cycle  cycle 2        2026, cycle  cycle 1        2026, cycle            
  after         2                           3                           2                      
  settlement                                                                                   
  cycle 3                                                                                      
  begins but                                                                                   
  USM Complete                                                                                 
  not yet                                                                                      
  received                                                                                     

  Payment       Tuesday 03   Tuesday 03     Wednesday 04 Tuesday 03     Wednesday 04 Rule 3    Correct
  arrives after February     February 2026, February     February 2026, February               
  USM Complete  2026, cycle  cycle 2        2026, cycle  cycle 2        2026, cycle            
  for cycle 2   2                           3                           3                      
  has been                                                                                     
  received                                                                                     
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## Settlement Cycle 3 to Settlement Cycle 1 Boundary (Monday to Thursday)

  ------------------------------------------------------------------------------------------------------
  Scenario      Payment      Derived        Current      Latest USM 979 Assigned     Rule      Outcome
  description   scheme       accounting     accounting   Complete       accounting   Applied   
                settlement   settlement     settlement   accounting     settlement             
                date and     date and cycle date and     settlement     date and               
                cycle        (from payment) cycle        date and cycle cycle                  
  ------------- ------------ -------------- ------------ -------------- ------------ --------- ---------
  Payment from  Monday 02    Tuesday 03     Tuesday 03   Tuesday 03     Tuesday 03   Rule 2    Correct
  settlement    February     February 2026, February     February 2026, February               
  cycle 3       2026, cycle  cycle 3        2026, cycle  cycle 2        2026, cycle            
  arrives just  3                           1                           3                      
  after 7:00 AM                                                                                
  but before                                                                                   
  USM Complete                                                                                 

  Payment from  Monday 02    Tuesday 03     Tuesday 03   Tuesday 03     Tuesday 03   Rule 3    Correct
  settlement    February     February 2026, February     February 2026, February               
  cycle 3       2026, cycle  cycle 3        2026, cycle  cycle 3        2026, cycle            
  arrives after 3                           1                           1                      
  USM Complete                                                                                 
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## Friday Settlement Cycle 3 to Monday Settlement Cycle 1 Boundary

  ------------------------------------------------------------------------------------------------------
  Scenario      Payment      Derived        Current      Latest USM 979 Assigned     Rule      Outcome
  description   scheme       accounting     accounting   Complete       accounting   Applied   
                settlement   settlement     settlement   accounting     settlement             
                date and     date and cycle date and     settlement     date and               
                cycle        (from payment) cycle        date and cycle cycle                  
  ------------- ------------ -------------- ------------ -------------- ------------ --------- ---------
  Friday        Friday 06    Monday 09      Monday 09    Friday 06      Monday 09    Rule 1    Correct
  settlement    February     February 2026, February     February 2026, February               
  cycle 3       2026, cycle  cycle 3        2026, cycle  cycle 2        2026, cycle            
  payment       3                           3                           3                      
  received                                                                                     
  during                                                                                       
  weekend                                                                                      
  window                                                                                       

  Friday        Friday 06    Monday 09      Monday 09    Friday 06      Monday 09    Rule 2    Correct
  settlement    February     February 2026, February     February 2026, February               
  cycle 3       2026, cycle  cycle 3        2026, cycle  cycle 2        2026, cycle            
  payment       3                           1                           3                      
  received                                                                                     
  Monday                                                                                       
  morning                                                                                      
  before USM                                                                                   
  Complete                                                                                     

  Friday        Friday 06    Monday 09      Monday 09    Monday 09      Monday 09    Rule 3    Correct
  settlement    February     February 2026, February     February 2026, February               
  cycle 3       2026, cycle  cycle 3        2026, cycle  cycle 3        2026, cycle            
  payment       3                           1                           1                      
  received                                                                                     
  after USM                                                                                    
  Complete                                                                                     
  ------------------------------------------------------------------------------------------------------

------------------------------------------------------------------------

## Long Delay Due to Sanction Checks

  --------------------------------------------------------------------------------------------------------
  Scenario        Payment      Derived        Current      Latest USM 979 Assigned     Rule      Outcome
  description     scheme       accounting     accounting   Complete       accounting   Applied   
                  settlement   settlement     settlement   accounting     settlement             
                  date and     date and cycle date and     settlement     date and               
                  cycle        (from payment) cycle        date and cycle cycle                  
  --------------- ------------ -------------- ------------ -------------- ------------ --------- ---------
  Payment delayed Tuesday 03   Tuesday 03     Thursday 05  Wednesday 04   Thursday 05  Rule 3    Correct
  two days due to February     February 2026, February     February 2026, February               
  sanction checks 2026, cycle  cycle 2        2026, cycle  cycle 3        2026, cycle            
                  2                           1                           1                      

  Payment delayed Monday 02    Tuesday 03     Thursday 05  Wednesday 04   Thursday 05  Rule 3    Correct
  three days from February     February 2026, February     February 2026, February               
  settlement      2026, cycle  cycle 3        2026, cycle  cycle 3        2026, cycle            
  cycle 3 due to  3                           2                           2                      
  sanction checks                                                                                

  Payment delayed Friday 06    Monday 09      Wednesday 11 Monday 09      Wednesday 11 Rule 3    Correct
  across weekend  February     February 2026, February     February 2026, February               
  due to sanction 2026, cycle  cycle 3        2026, cycle  cycle 3        2026, cycle            
  checks          3                           1                           1                      

  Payment delayed Monday 02    Monday 02      Monday 23    Friday 20      Monday 23    Rule 3    Correct
  multiple weeks  February     February 2026, February     February 2026, February               
  due to sanction 2026, cycle  cycle 1        2026, cycle  cycle 3        2026, cycle            
  investigation   1                           1                           1                      
  --------------------------------------------------------------------------------------------------------
