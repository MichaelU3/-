## How to config SourceTree to connect to Github

### SSH

1. Create SSH keys in SourceTree

> Tools -> Create or Import SSH Keys
>
> 1. check "EdDSA" in Parameters. Default is "RSA", which is a old version that Github does not support any more.
>
> 2. Click Generate to generate keys.
>
> 3. Click "Save public key" to save public SSH key
>
> 4. Key -> Parameters for saving key files... -> check "2" in PPK file version -> OK. *version 3 is a higher version that SourceTree does not support.*
>
> 5. Clic "Save private key" to save private SSH key

![PuTTY Key Generator!](https://img-blog.csdnimg.cn/4d53957de3264788bd9771cfd4d1378a.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAbGlzaHVhbmdxdWFuMTk4Nw==,size_10,color_FFFFFF,t_70,g_se,x_16)

![PuTTY Key Generator 2!](https://i0.wp.com/mulcas.com/mulcas_uploads/2021/12/Couldnt-load-private-key-Putty-key-format-too-new-mulcas2106002.png?ssl=1)

![PuTTY Key Generator 3!](https://i0.wp.com/mulcas.com/mulcas_uploads/2021/12/Couldnt-load-private-key-Putty-key-format-too-new-mulcas2106003.png?ssl=1)

2. Log in GitHub

> User profile -> Setting
>
> 1. Click "SSH and GPG keys" at left navigation section
>
> 2. Click "New SSH key" to add a new key
>
> 3. Specify any name, that open public key just saved, copy contents and paste in GitHub window
>
> 4. Save the key

3. Clone repository in local disc

> if SourceTree ask for any configuratio in "Pageant", go to system processes to find it.
>
> Clone repository

![launch Pageant!](https://img-blog.csdnimg.cn/a7612499c25746fe974d5023827a6d3a.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAbGlzaHVhbmdxdWFuMTk4Nw==,size_11,color_FFFFFF,t_70,g_se,x_16)

### Errors

1. Couldn't load private key - Putty key format too new

> [resolve](https://mulcas.com/couldnt-load-private-key-putty-key-format-too-new/)

![error screenshot!](https://www.itcan.cn/wp-content/uploads/2021/09/1.png)

2. You’re using an RSA key with SHA-1, which is no longer allowed

> [resolve](https://blog.csdn.net/lishuangquan1987/article/details/123588802)

![Error screenshot!](https://img-blog.csdnimg.cn/8bc8587c47d84131a47f086be213d999.png?x-oss-process=image/watermark,type_d3F5LXplbmhlaQ,shadow_50,text_Q1NETiBAbGlzaHVhbmdxdWFuMTk4Nw==,size_17,color_FFFFFF,t_70,g_se,x_16)


