Redis:

    #Run Redis client
        redis-cli

    #Connect to the server using client redis-cli
        redis-cli -h host -p port -a password
            #Options include.
                -h = hostname
                -p = portname
                -a = password

    #Delete Command
        DEL KEY_NAME

    #Dump Command
        DUMP KEY_NAME

    #Exists Command
        EXISTS KEY_NAME

    #Expire Command
        Expire KEY_NAME TIME_IN_SECONDS

    #Expireat Command
        Expireat KEY_NAME TIME_IN_UNIX_TIMESTAMP

    #Pexpire Command
        PEXPIRE KEY_NAME TIME_IN_MILLISECONDS

    #Pexpireat Command
        PEXPIREAT KEY_NAME TIME_IN_MILLISECONDS_IN_UNIX_TIMESTAMP

    #Keys Command
        KEYS PATTERN

    #Move Command
        MOVE KEY_NAME DESTINATION_DATABASE

    #Persist Command
        PERSIST KEY_NAME

    #TTL Command
        TTL KEY_NAME 

    #Random key Command
        RANDOMKEY

    #Rename Command
        ENAME OLD_KEY_NAME NEW_KEY_NAME

    #Type Command
        TYPE KEY_NAME

    #Set Command
        SET KEY_NAME VALUE

    #Get Command
        GET KEY_NAME

    #Getrange Command
        GETRANGE KEY_NAME start end

    #Getset Command
        GETSET KEY_NAME VALUE

    #Mget Command
        MGET KEY1 KEY2 .. KEYN

    #Setbit Command
        SETBIT KEY_NAME OFFSET

    #Strlen Command
        STRLEN KEY_NAME

    #Mset Command
        MSET key1 value1 key2 value2 .. keyN valueN

    #Incr Command
        INCR KEY_NAME
    
    #Decr Command
        DECR KEY_NAME

    #Append Command
        APPEND KEY_NAME NEW_VALUE

    #Select Command
        SELECT DB_INDEX

    #Quit Command
        QUIT
    
    #Ping Command
        PING

    #Echo Command
        ECHO "Redis database"

    #Auth Command
        AUTH PASSWORD

    #Exec Command
        EXEC

    #Discard Command
        DISCARD

    #Append Command
        APPEND KEY_NAME NEW_VALUE

    #Decrby Command
        DECRBY KEY_NAME DECREMENT_AMOUNT

    #Incrby Command
        INCRBY KEY_NAME INCR_AMOUNT
