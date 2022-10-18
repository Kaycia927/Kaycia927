import random
import string
import asyncio

async def get_random_string(length):
    # choose from all lowercase letter
    letters = string.ascii_uppercase
    result_str = ''.join(random.choice(letters) for i in range(length))
    print(result_str)
    
async def my_function1():
  print(random.randint(0,9))
  
async def my_function2():
  print(random.randint(100,999))
  
async def my_function3():
  print(id(object))


if __name__ == "__main__":
   loop = asyncio.get_event_loop()
   loop.run_until_complete(asyncio.gather(my_function1(), get_random_string(3),\
   my_function2(), get_random_string(4), my_function3()))
