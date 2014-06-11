Habibi API
===========================


* [Matches service](#matches)
* [Near Me](#near-me)
* [Submit plan](#submit-plan)
* [Update statment](#update-statment)



## matches

**Request**

* MyLikes :
    * GET http://habibi/api.php/matches?id=1&type=1&page=1
* LikesMe:
    * GET http://habibi/api.php/matches?id=1&type=2&page=1
* LikesMe:
    * GET http://habibi/api.php/matches?id=1&type=3&page=1
    
**Response Example**

    {
        status: "success",
        data: [
            {
                id: "53",
                name: "Quamar",
                age: "23",
                country: null,
                city: null,
                gender: "Male"
            },
            {
                id: "51",
                name: "Derek",
                age: "23",
                country: null,
                city: null,
                gender: "Male"
            },
            {
                id: "69",
                name: "Shelly",
                age: "23",
                country: "American Samoa",
                city: "`ali khel",
                gender: "Male"
            },
            {
                nb: "3"
            }
        ]
    }

## Near Me

>**Note**

>user_id: required

>page: not required , default page = 1 , 30User/page 

>dist: distance filter(KM), not required, default 100.

**Request**

    http://habibi/api.php/nearMe?page=2&user_id=1&dist=90

    
**Response Example**

    {
        data: [
            {
                id: "3",
                first_name: "Vanna",
                filename: ""
            },
            {
                id: "4",
                first_name: "Henry",
                filename: "http://habibi/photos/thumbnails/bbbbb"
            }
        ],
        status: "success"
    }
    

## Submit Plan

*Request*

    * POST http://habibi/api.php/submitPlan.json   content:{"apikey":"7abibi", "identifier":"mobi.app4mob.plan.chat-2j", "user_id":"1" }
  
*Response*

     {"status":"success","data":null}
     {"status":"fail","data":{"identifier":"This plan doesn't exist"}}
     {"status":"fail","data":{"apikey":"Invalid apikey"}}
     {"status":"error","data":"An exception was thrown"}
     {"status":"error","data":"content not valid"}
     
## Update Statment

*Request*

    * POST http://habibi/api.php/editStatment.json   content:{"apikey":"7abibi","statement":"This is my statement", "user_id":"15" }
  
*Response*

     {"status":"success","data":null}
     {"status":"fail","data":{"statement":"statement is required"}}
     {"status":"error","data":"content not valid"}
        
