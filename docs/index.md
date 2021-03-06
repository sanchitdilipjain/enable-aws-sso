## Enable AWS SSO

**Introduction**

- Access management across different AWS accounts is a complicated and painful task but now with AWS SSO, it is much easier and simple to handle such activities. In this tutorial, we will focus on configuring AWS SSO to simplify user management across multiple accounts based on their roles.
- This tutorial is divided into sections
    
    1. Switch AWS SSO for your organization
    2. Configure AWS SSO permission sets
    3. Configure AWS SSO groups
    4. Allocate groups to your accounts
    5. Customize your SSO endpoint
    6. Connect to the AWS Console using your SSO endpoint

**Tutorial**

- Step 1. Switch AWS SSO for your organization

    1. Go to the <a href="https://console.aws.amazon.com/singlesignon/home"> AWS SSO home page </a>
       
       <img src="images/image1.png" class="inline"/>
    
    2. Select Enable AWS SSO
       
       <img src="images/image2.png" class="inline"/>
    
    3. Wait for AWS SSO to be enabled
       
       <img src="images/image3.png" class="inline"/>
    
    4. After SSO is switched, we will be navigated back to the SSO Dashboard and with a success message displayed.

       <img src="images/image4.png" class="inline"/>

- Step 2. Configure AWS SSO permission sets

    1. Select the AWS accounts section
       
       <img src="images/image5.png" class="inline"/>
    
    2. Go to the Permission sets tab and click Create a permission set
       
       <img src="images/image6.png" class="inline"/>
    
    3. Choose to Use an existing job function policy and click Next: Details 
       
       <img src="images/image7.png" class="inline"/>
    
    4. Select AdministratorAccess job function policy and click Next: Tags

       <img src="images/image8.png" class="inline"/>
       
    5. Select Next: Review :

       <img src="images/image9.png" class="inline"/>

    6. You can also modify the session duration and this will affect the amount of time a user can use the AWS Console or CLI before being automatically logged out. Otherwise, click Create to finalize the creation of the permissions set

       <img src="images/image10.png" class="inline"/>

    **Note:** You can repeat the above steps to define the other roles

- Step 3. Configure AWS SSO groups

    1. Select on the Groups Tab in the AWS SSO console
       
       <img src="images/image11.png" class="inline"/>
    
    2. Click Create group
       
       <img src="images/image12.png" class="inline"/>
    
    3. Type Administrators as the group name and click Create 
       
       <img src="images/image13.png" class="inline"/>

    **Note:** You can repeat the above steps to define the groups for other roles

- Step 4. Allocate groups to your accounts

    1. Select the AWS Accounts section in the AWS SSO console
       
       <img src="images/image14.png" class="inline"/>
    
    2. Check all your accounts and click Assign users
       
       <img src="images/image15.png" class="inline"/>
    
    3. Navigate to Groups tab, select Administrators group, and click Next: Permissions set
       
       <img src="images/image16.png" class="inline"/>
    
    4. Mark AdministratorAccess permissions set and click Finish

    5. Wait until all selected accounts are being configured
    
    6. Once it is completed, select on Proceed to AWS accounts 

    **Note:** You can repeat the above steps for the other roles

- Step 5. Customize your SSO endpoint

    1. Navigate to the AWS SSO page and at the bottom of the page, select the Customize link
       
       <img src="images/image17.png" class="inline"/>
    
    2. Provide your domain name and click Save
       
       <img src="images/image18.png" class="inline"/>
    
    3. Now you can login to the AWS Console through your SSO portal using your customized URL

- Step 6. Connect to the AWS Console using your SSO endpoint
    
    1. Select the Users section in the AWS SSO console
       
       <img src="images/image19.png" class="inline"/>
    
    2. Click Add user
       
       <img src="images/image20.png" class="inline"/>
    
    3. Provide details in the form like 

        - Username 
        - Password (Steps to setup password / One time password)
        - Email address
        - First Name
        - Last Name
        - Display Name
        
       Once the form is completed, click Next Groups
       
       <img src="images/image21.png" class="inline"/>

    4. Select the Administrators group created previously and click Add user
    
       <img src="images/image22.png" class="inline"/>
    
    5. Check your email and Accept the invitation
      
       <img src="images/image23_1.png" class="inline"/>
       
       **Note** In case if you select a One-time password while providing user details then you need to copy the below confirmation message with the password and share it offline with the user
    
       <img src="images/image23_2.png" class="inline"/>
    
    6. You should be redirected to a page to set your password. Once you have set your password, click Update user  
    
       <img src="images/image24.png" class="inline"/>
   
    7. Once your account is successfully activated, click Continue
    
    8. Click the AWS Account card to expand the list of accounts
        
       <img src="images/image25.png" class="inline"/>
    
    9. Click on your main account to view the access options for the account 
    
    10. Click on Management console to access your main account via the AWS Management Console
   
  You are now connected as your new SSO Administrator user
  
  <img src="images/image26.png" class="inline"/>
