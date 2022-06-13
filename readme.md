
# Gamil-api

Send Email with the Gmail API and Node.js


### 1) Create a Google Cloud Project
Go to ****cloud.google.com**** and create a new Google Cloud project. Give your project a name, and click the Create button.

 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28643833-a93f208fbdd80653ece3c7ce419f7215.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T103945Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=2972bd8fa1e0af1115fc39390402af7931fa077567e5f2b35e01602c03c89f48)
### 2) Configure OAuth Consent Screen
Under the **APIs and Services** section, click on *OAuth Consent Screen* and set the user type as External and Click on create button.

 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28643907-fd8c24f75177b7e70b9907c2eaff0248.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T103920Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=07492706475511a72f985a3fa353d1caccca3abaa91801277e775ddaffa140d7)




###  3) Oauth consent screen  
In that screen you need following information
- App information ----> App-name
- App information ----> User support email
- Developer contact information ----> Email address
 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644032-b09947d579df5d21a82fb6283775ce64.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T104159Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=c66dfff39c4a520376f51c7c11848da1da7c6b2e90dacd638c2c0b97864c8ee3)


 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644111-812a7aa1faadf15474831427530a7f1f.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T104321Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=227d0fc92ff1276787f58c97d1e8d698a9186e300a21e8ec477247f6424f2778)



### 4) Create Gmail OAuth Client
In the **APIs & Services** section, click on *Credentials* and click on Create credentials > OAuth Client Id to create a new client ID that will be used to identify your application to Google’s OAuth servers
 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644183-09914b85e849e733b6983374ede7d8f5.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T104451Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=6bd2c0c0c69fc1444081d84bcbb9019f630fac49ecf80481cc61a719010798d0)
 
### 5) Application Type
Set the application type to Web application App, give your OAuth Client a recognizable name and in Authorized redirect URIs add **https://developers.google.com/oauthplayground**  then click Create to generate the credentials.

 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644248-5c6b0413e46b46ac03c5d2e304a50930.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T104606Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=762013ff5401928e21227ce515d5fb892ef558e3f39969e0e5e75990da07eb45)
 
### 6) Open https://developers.google.com/oauthplayground in new tab.
In top right corner there is one setting icon click on that. after clicking you will see pop-up. in that pop-up you need to check-box at down corner **Use your own OAuth credentials. Fill client ID and client screte ID in that input fileds.Now close tha pop-up. Select step - 1 **Select & authorize APIs** in that input filed add **https://mail.google.com**. click on authorize APIs button.
 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644354-629d6be5f42a56993928cba716f8121d.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T104826Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=22c317f5ede7feb6453f1fad0ba757a27e2b07f7167679e9dfb6c7ab05af1df0)


### 7) Select test account user that added in that Oauth consent screen.
 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644433-f45e681f31622ed617a11a500fe5d9a5.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T104939Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=c65b4e27ec5734f889aed24f8dc45a46cc0177b58406c1959bad76a833509317)
 
### 8) Click on continue.
 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644466-63183c3ae3b559e63cbbdc85396d4af2.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T105028Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=113a928389ec5dec4e12a9dc382cb438d3934e51e14231017a53909ad4f186a3)

### 9) Click on continue than it will be redirect into **https://developers.google.com/oauthplayground**.
 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644502-18cdde862b7d7e2eefaf15a24a9434e7.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T105057Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=947861deaf87be26a7bfa126b81e412949cd43a628cc15a7595cd14064f65ee5)


### 10) Refresh token
In step 2 click on Exachange authorization code for tokens button 
 ![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644563-8b14405e115fb3043959df3354bd0999.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T105202Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=d6842669e256e9865fcecc3107add2aa77f90c5756c6227df0944376c40eca67)


### 11) Get refresh token.
![Alt Text](https://awesomescreenshot.s3.amazonaws.com/image/3415276/28644596-ac282f664251bd71a1464a4a4a7a1271.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAJSCJQ2NM3XLFPVKA%2F20220613%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20220613T105247Z&X-Amz-Expires=28800&X-Amz-SignedHeaders=host&X-Amz-Signature=f9a7c6a58faa45bba243ac610cf9702eab042c4f8d48cb9928918de3f02147d5)

- Client ID, Client screte ID and refresh token ----> Add into environment file and use into node-app.






