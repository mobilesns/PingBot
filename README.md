# PingBot
A bot sending messages to a room running on Symphony Platform

Features:
- PingBot sends a message to a room every 5 minutes.
- Pingbot sends a message to a room at the start of everyday and @mention a list of users.
- There is an additional payload containing random alphabet and numbers placed in card of Symphony messageML.
- The size of the additional payload changes at the start of everyday with the order 1000 -> 5000 -> 10000 -> 20000 -> 40000 -> 1000 ...... and on and on.
- The size of the message and payload are shown in a message.

Commands:
- /msg : Set message that will be sent to a room. If this command is not executed the message will be empty. 
- /test : Start sending messages to a room.
- /stop : Stop sending messages to a a room.

Please execute the /msg command before the /test command.

After stopping the message sending by the /stop command the /msg and /testcommands can be exectued again.

In the top directory:
- Clean and build PingBot - $mvn clean install dependency:copy-dependencies
- Run PingBot - $java  -classpath target/dependency/*:target/classes PingBot

Add PingBot to any room then execute the  /msg and /test commands to start sending messages to the room.
