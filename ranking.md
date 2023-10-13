```mermaid
sequenceDiagram
    actor user
    user->>+Statistics:From Home Page click on Ranking menu redirected to one  hour tab(/statictics)

    Statistics -->>+MPC B: /collections/statistics-top?sortBy=one_hour
    Note over Statistics,MPC B:Method Get 
    MPC B -)-Statistics:Response

    user->>+Statistics:From Home Page click on Ranking menu redirected to one hour tab<br/> click on dropdown menu for 6 ,24 hours and 7 days statistics

    Statistics -->>+MPC B: /collections/statistics-top?sortBy=six_hour
    Note over Statistics,MPC B:Method Get 
    MPC B -)-Statistics:Response
    
    user->>+Statistics:From Home Page click on Ranking menu click on 24 hour trend tab

    Statistics -->>+MPC B:/nft-collections/statistics-trending?
    Note over Statistics,MPC B:Method Get 
    MPC B -)-Statistics:Response

```