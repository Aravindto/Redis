# Redis-tips
## REDIS Comment 
	- To Start - redis-cli
	- To Exit - exit
	- To Insert Key and Value - SET KEY VALUE (Ex - SET Name Ben)
	- To Get the value - GET KEY (Ex - GET Name)
	- To Get all - keys *
	- To Delete - DEL KEY (EX - DEL Name)
	- To check if the value exists - EXISTS KEY (EX - EXISTS Name) returns(1 if it exists 0 if not exists)
	- To delete all = FLUSHALL
	
## TTL - Time to Live (-1 No Expiration, -2 It's gone)
	- To MAke the key Expire - EXPIRE KEY (EX - EXPIRE Name 10(seconds))
	- To check the time - TTL KEY (TTL Name)
	- To Set the time to expire - SETEX Key Seconds Value (EX - SETEX Name 10 Ben)
	
## To Store it as List
	- LPUSH KEY VALUE (EX - LPUSH Name Ben)(To store the value in left side(FIRST) of the list)
	- To Push the list in right side(END) LPUSH KEY VALUE (EX - RPUSH Name Bobby)
	- To Get list LRANGE KEY (Range Start(0),Range End(-1)) (EX - LRANGE Name 0 -1)
	- To Pop the list in left side(FIRST) LPOP KEY (EX - LPOP Name)
	- To Pop the list in right side(LAST) RPOP KEY (EX - RPOP Name)
	
## To store Sets(Unique)
	- To Push SADD hobbies "Weight lifting"
	- To Get SMEMBERS hobbies
	- To Remove SREM hobbies "Weight lifting" 
	
## To Store as Hash SET
	- To Push HSET KEY FIELD VALUE (EX - HSET person name John)
	- To Get HGET KEY FIELD (EX - HGET person name)
	- To Get All HGETALL KEY (EX - HGETALL person )
	- To Delete HDEL KEY FIELD (EX - HDEL person name)
	- To Check if it exists HEXISTS KEY FIELD (EX - HEXISTS person name)