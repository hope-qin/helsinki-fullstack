```mermaid
---
title: [Single Page App]
---
---
title: Single Page App
---
flowchart TD
    subgraph Browser
        requestHTML[Request HTML from Server] --> requestLoadJS[Request & Load JS File] --> executeJS[Execute JS, Initialize Elements & Processing] --> B{User Input}
        subgraph JScode[JS Code]
            B --> fetchingInput[Fetching Input Elements] --> registerEvent[Register an Event to Dual Program] --> C[Running with User's Execute]
        end
        subgraph Server
        C --> stayCurrentPage[Stay on Current Page, Local Update]
        C --> receiveHTTPPost[Receive HTTP POST] --> parseJSON[Parse JSON Data] --> storeNote[Store Note] --> respondResult[Respond the Result to Client]
        end
    end



```