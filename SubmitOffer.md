```mermaid
sequenceDiagram
    actor user
    user->>+Asset:From Home Page click on any album or asset -><br/> Click on send offer()
    Asset -->+Send offer:/asset/{assetId}
    Send offer ->>+MPC B: /nft-contents/796/purchase-offers
    Note over Send offer,MPC B:Method Post 
     MPC B -)-Send offer:Response
    Send offer ->>+MPC B: /nft-contents/796/purchase-offers?take=10
    Note over Send offer, MPC B:Method Get
    MPC B -)-Send offer:Response
```