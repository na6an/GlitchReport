# Account Redundancy
### Related service providers: Amazon, Verizon  
## Background:
It was my first time using AWS earlier this year.  
I heard about AWS, but never had a chance to use it until recently when I began to learn deep learning.  
The problem was, my ThinkPad had no GPU. So, I started using EC2 service on AWS.

Then, I ran into a strange issue.  
  <img src="https://github.com/na6an/GlitchReport/blob/master/img/aws-login.PNG" alt="alt text" width="480" height="320">  
Whenever I tried to login, It comes back to this “Create an AWS account” page no matter what I do.  
Attempting to create new account or clicking sign in to an existing account didn’t help me escape from the page loop.

The only possible solution was not using AWS.  
I contacted AWS customer service and received following letter.

  <img src="https://github.com/na6an/GlitchReport/blob/master/img/aws-inquiry.png" alt="alt text" width="800" height="320"> 

## Root Cause:
According to this e-mail, I have two Amazon.com accounts with same e-mail.  
I soon realized what might have caused the problem.

  <img src="https://github.com/na6an/GlitchReport/blob/master/img/amz-diagram.png" alt="alt text" width="640" height="250">  

The original e-mail I used for Amazon.com account was hotmail e-mail,   
and I changed it to gmail e-mail address some time last year.  
This must have conflicted with existing AWS account that I created using gmail   
because of the unified login for AWS and other amazon services.

This means, Amazon’s unified login system conflicts with my e-mail change.

I cannot tell whether this is the true cause or not because I’m not an Amazon employee.  
But it became clear this hypothesis was the likely when I verified my e-mail with the link they provided.  
It caused another problem - not with AWS account, but Amazon.com account.  
Apparently the account that AWS customer service has removed was tied with my amazon store account.  
I have business prime membership and my account was all reset after verifying with the link  
-  removing my membership status, purchase history, etc.

Then, I had to contact Amazon.com customer service to restore the access to the account.  
Now I came back to square one, still having the issue of page loop from duplicate account.  
