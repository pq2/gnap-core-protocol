+--------+                                  +--------+          .----.
| Client |                                  |   AS   |         | User |
|Instance|                                  |        |         |      |
|        |<=(1)== Start Session ===============================+      |
|        |                                  |        |         |      |
|        +--(2)--- Request Access --------->|        |         |      |
|        |                                  |        |         |      |
|        |<-(3)-- Interaction Needed -------+        |         |      |
|        |                                  |        |         |      |
|        +=(4)== Redirect for Interaction ====================>|      |
|        |                                  |        |         |      |
|        |                                  |        |<==(5)==>|      |
|        |                                  |        |  AuthN  |      |
|        |                                  |        |         |      |
|        |                                  |        |<==(6)==>|      |
|        |                                  |        |  AuthZ  |      |
|        |                                  |        |         |      |
|        |<=(7)== Redirect for Continuation ===================+      |
|        |                                  |        |          `----`
|        +--(8)--- Continue Request ------->|        |
|        |                                  |        |
|        |<-(9)----- Grant Access ----------+        |
|        |                                  |        |
|        |                                  |        |     +--------+
|        +--(10)-- Access API ---------------------------->|   RS   |
|        |                                  |        |     |        |
|        |<-(11)-- API Response ---------------------------|        |
|        |                                  |        |     +--------+
+--------+                                  +--------+
