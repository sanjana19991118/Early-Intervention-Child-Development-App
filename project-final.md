# REGISTRATION # LOGIN  # ACCOUNT
# User (ADMIN /PARENT/DOCTOR) 
>_id
> username 
> Email Id 
> Password 
> Role [admin,parent,doctor]

# Parent  details 
>_id
> image
> Phone Number 
> userId
> Address
> Age
> City
> State
> Qualification 


# DOCTOR / SPECIAL EDUCATORS 
>_id
> userId
> image
> Phone Number 
> Address
> City 
> State 
> Designation 
> Education (RCI certificate - Boolean [ true / false ]) - 
     array of objects ( 1.title 2.college )
> Experience
> Achievements  
    array of Object - (1. title 2. Board/Org)
> Language  
    array of string

# CONDITIONS (HOME)
>_id
> image 
> disabilityName  (condition)  
> body


<!-- # ABOUT US 
_id
> title
> video -->  

# Paitent
 name 
 age
 height
 weight
 symptoms
 parent 

# CHECKLIST 
_id
> userId ( doc / admin )
> Pointers 
> Symptoms ( array of Object 1. title)
> Status /Options [often, rarely, always]  and [E , G , I , D , C , P] [ { name: 'often', points:3 }, { name: 'rarely', points: 2, ... }]


# CheckList response 
_id 
> checklist id 
> parentId 
> Symptoms ( array of objects = 1. symptonId, 2. optionId)
> 


version 2
# GAMES (dynamic) 
_id 
<!-- > file upload -->
> text [enum]
> image 
> Audio
> video 
<!--Table,text, -->


