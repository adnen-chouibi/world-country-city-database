Habibi API
===========================


* [Matches service](#matches)
* [Submit plan](#submit-plan)



## matches
* MyLikes :
    * GET http://habibi/api.php/matches?id=1&type=1&page=1
* LikesMe:
    * GET http://habibi/api.php/matches?id=1&type=2&page=1
* LikesMe:
    * GET http://habibi/api.php/matches?id=1&type=3&page=1
    
*Response Example*

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

## Submit Plan

*Request*

    * POST http://habibi/api.php/submitPlan.json   content:{"apikey":"7abibi", "identifier":"mobi.app4mob.plan.chat-2j", "user_id":"1" }

*Response*

    * Success:

    {"status":"fail","data":{"identifier":"This plan doesn't exist"}}    
