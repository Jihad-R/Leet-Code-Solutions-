# Leet-Code-Solutions-
Note that I am not a Genius. I just wanted to share my solutions for  some leet code questions. Maybe this can help someone and that would make me happy :)


#   Max Consecutive Ones {Easy}
This problem basically wants us to find the greatest number of consecutive ones in an array. Consecutive means one after the other btw.  

For example this array --> [1,0,1,1,0,1] has **2** consecutive ones [1,0,**1**,**1**,0,1].

## Solution

I am a beginner with this competitve programming ordeal and most of my solution are quite naive. But I feel the approach we will be using for this problem is fairly efficent when compared to our skill level. First I will post the code block then we can go step by step to explain it. 


### Java Solution 

    public int findMaxConsecutiveOnes(int[] nums) {
        
        int max =0;  # this variable holds the maximum number of consecutive ones in an array 
        int current = 0; # this variable keeps track and increments everytime there is a series of ones
        
        for(int n : nums){  # Don't get scared this line just gives us an easy for loop that we can work with
                            # it is not your conventional for loop but if you have ever coded in python it is very similar...
                            # to the for loop in python it basically means for every element (n) in the array (nums)
                            # meaning that n is the element and we don't need to use the index syntax (array[index]) to grab the elements in an array
                            # we can simply use n to grab the element using this special for loop syntax
                            # I hope that is clear 😅
                            
            if(n == 1)      # Now we check if n is equal
            {
                current++; # incase the condition is true we increment the current variable by 1 
                max = Math.max(current, max); # then we compare it with the max number of 1s we currently have, since this is our 
                                              # first trial the max = 0 and the current variable has been incremeanted by one the new value of
                                              # max will be 1 and this comparison keeps on happening every time we incounter a 1
            }
            else  # Now the fun part is here when we incounter a number that is not a one the following happens
            {                 
                current = 0; # The current variable we used to track the number of ones becomes zero. This makes sense because we are looking for consecutive
                             # ones and since we incounter a number that is not one we should reset our current variable.
            }
        }
        
        # we do this until we traverse the whole array leaving us with an linear time complexity O(N) 
        
        return max;
        
    }
    }

If you can't understand my writing style or what I just wrote please watch this video down below that explains how to solve this problem.

[Youtube Video Solving the Consecutive Ones Problem](https://youtu.be/PLa4tYQhqoU)  <--- Click Link to watch video

I have also provided the solution in python code for anyone who is interested.  It is esstentially the same thing as the Java solution but just in different syntax


### Python Solution


        current = 0
        max_num = 0
        
        for i in nums: 
            if(i == 1):
                current+=1
                max_num = max(current,max_num)
                
            else:
                current = 0
                
        return max_num


#   Palindrome Number {Easy}

Given an integer x, return true if x is palindrome integer.

An integer is a palindrome when it reads the same backward as forward.

For example, 121 is a palindrome while 123 is not

This is probably the easiest question I have come across so far. It is especially easy because I was aware of the built in functions and methods provided by the python programming language. Here are the **Runtime** and **Memory Usage** details of my solution.

Runtime: 38 ms, faster than 99.62% of Python3 online submissions for Palindrome Number.
Memory Usage: 14.2 MB, less than 78.46% of Python3 online submissions for Palindrome Number.

    def isPalindrome(self, x: int) -> bool:
        
        x = str(x) // convert the input to a string
        
        return x[::-1] == x //return the comparison between the inverted string and the original string (either true or false)
        
I utilized my knowledge of arrays and strings in python to come up with the solution. It was such a no brainer more notably because the problem had no constraints on how to solve it. We first convert the integer input (x) into a string using the **str** (string parsing) method. Then we simply inverse the string using the following syntax *x[::-1]*. This is becuase we can index string characters in python the same way we can index array elements. This gives us great flexiblity to work with and manipulate strings. So after inverting the string we just simply compare it with the original string. Then  finally, if it is the same return true and if it is not the same return false. Simple. I feel like I cheated on this one honestly but it was fun to do. 
        


Thanks for reading and if you understood something then celebrate 🎉🎉🎉🎉

<p align="center">
  <img src="https://thumbs.gfycat.com/AllBabyishAardvark-max-1mb.gif" alt="Kodak Black Dance"/>
</p>

