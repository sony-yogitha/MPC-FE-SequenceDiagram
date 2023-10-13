```mermaid
sequenceDiagram
    actor user
    participant H as Home
    participant M as Market
    participant A as Album/Work
    participant U as User
    participant B as MPC B
    user->>+H:From Home Page click on any Market 
    H ->>M:/search-result?tab=nft
    M->>+B: /nft-contents?page=1&type=filter
    Note over M,B:Method Get
    B -)-M:Response

    user ->>A:Click on Album from home page
    H->>A:/search-result?tab=album
    A->>+B:/nft-collections?page=1
    Note over A,B:Method Get
    B-)-A:Response


    H ->>A:Click on Album or Market from home page a Tab for user is navigated
    A->>U:/search-result?tab=user
    U->>+B:/artists?page=1
    Note over U,B:Method Get
    B-)-U:Response



```