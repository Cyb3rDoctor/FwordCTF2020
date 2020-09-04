# Identity Fraud (OSINT - 500 points)

![-000](https://user-images.githubusercontent.com/70543460/92163537-8c72be80-ee3c-11ea-8fbb-2a5e186eb941.png)

<br/><br/>

-----

# Solution:

You have a twitter account in the description, open it and you will see tweet replies that are related to what is explained in the challenge description.
<br/><br/>
```
General obvious note:

Some of the players told me that there is a technical problem and they can’t see all the tweet replies, but I mentioned that (Eword) has replied to the fake account, so you need to check Eword twitter account too to see all the replies. (You’ll find Eword account in the replies of the fake account, also in the following list of the fake account)
```
![-001](https://user-images.githubusercontent.com/70543460/92163821-f7bc9080-ee3c-11ea-91ba-be2261eed584.png)

![-003](https://user-images.githubusercontent.com/70543460/92163845-01de8f00-ee3d-11ea-8f8f-918eccbee8d4.png)

```
The fake twitter account that I’ve mentioned in the description:
https://twitter.com/1337bloggs

Eword Team twitter account:
https://twitter.com/EwordTeam
```
<br/><br/>

-----

**So, here is the tweet and the replies to it:**

<br/><br/>
![tweet](https://user-images.githubusercontent.com/70543460/92232557-68a08e80-eeb7-11ea-99bf-7771b47f28bd.jpg)
<br/><br/>

-----

According to the description and the replies, there is a task that needs to be solved…
<br/><br/>
In one of the replies, Eword says that something will be in their CTFtime team page and will be deleted when Fred (the fake account) takes a screenshot of the CTFtime team page.

**Note:**
You can find Eword CTFtime page link in their twitter account.
<br/><br/>
![-009](https://user-images.githubusercontent.com/70543460/92164200-a06af000-ee3d-11ea-9e24-1826598e66d0.png)
<br/><br/>
```
https://ctftime.org/team/131587
```
<br/><br/>

When you open Eword CTFtime team page link, you won’t find anything interesting.
<br/><br/>
<kbd>
![-010](https://user-images.githubusercontent.com/70543460/92164243-b8427400-ee3d-11ea-8433-a9a635152c2b.png)
</kbd>
<br/><br/>

<br/><br/>
**That’s because Eword said in the reply that they will delete that thing from their CTFtime page.**
<br/><br/>

**So, you need to find that thing before it was deleted.**
<br/><br/>

...

<br/><br/>

One of the ways to find something deleted from a webpage is to check previous versions of that page…
<br/><br/>
**And simple “googling” will give you the method:**

![-011](https://user-images.githubusercontent.com/70543460/92164373-f17ae400-ee3d-11ea-9613-8c68c252cbb2.png)

<br/><br/>

So, using The Wayback Machine on the CTFtime page link will give you what are you looking for:

1. Go to https://archive.org/web/
2. Type the link of Eword CTFtime team page and click (browse history):
<br/><br/>
![-012](https://user-images.githubusercontent.com/70543460/92164441-05264a80-ee3e-11ea-889f-aea2f92547a6.png)
<br/><br/>

You’ll find previous versions of Eword CTFtime webpage:
![-013](https://user-images.githubusercontent.com/70543460/92164477-13746680-ee3e-11ea-8743-f2df0b15f1cc.png)
<br/><br/>

That one looks interesting, it has a Pastebin link.
<br/><br/>

Open it and you will find the task:
https://pastebin.com/8bk9qLX1

![-014](https://user-images.githubusercontent.com/70543460/92165208-5d118100-ee3f-11ea-8fc3-c49dfd51f956.png)

So, you need to find the leader of Eword team, and when you open the hint, you will find a base64 encoded image.
https://pastebin.com/PZvaSjA0

![-015](https://user-images.githubusercontent.com/70543460/92165313-84684e00-ee3f-11ea-85ca-83b4c6247dd2.png)

<br/><br/>

You can use CyberChef to know what that base64 encoded text will give you:
https://gchq.github.io/CyberChef/

![-016](https://user-images.githubusercontent.com/70543460/92165362-9b0ea500-ee3f-11ea-8ed6-7a7029858632.png)

![-017](https://user-images.githubusercontent.com/70543460/92165389-a792fd80-ee3f-11ea-9a16-e4fcc6552a55.png)

```
Note:
You can use different sites/methods to get the image.
I just explained one of the methods above.
```

<br/><br/>

This is the image that you will get:
<br/><br/>
![-019](https://user-images.githubusercontent.com/70543460/92165466-c8f3e980-ee3f-11ea-9987-74df23f1e007.png)

-----

**I put small clues in that image:**
<br/><br/>
![-020](https://user-images.githubusercontent.com/70543460/92165548-e45ef480-ee3f-11ea-88bd-83e70e0aa83a.png)
<br/><br/>
![-021](https://user-images.githubusercontent.com/70543460/92165573-ede85c80-ee3f-11ea-8fa6-1e12c4154b7e.png)

<br/><br/>
The words “Hotel” and “Advisor” aims to “Trip Advisor” site:

![-022](https://user-images.githubusercontent.com/70543460/92165629-022c5980-ee40-11ea-8db3-3197fcfd31eb.png)

<br/><br/>

**The intended way to continue solving this challenge:**
<br/><br/>
**Locate that hotel from the image that you got, then search for it in Trip Advisor site and look in the reviews of that hotel.**

```
Note:
I know that there is a shorter way to reach the review, but it’s unintended and it’s guessy, so I won’t mention it.
```

<br/><br/>

To locate the hotel, you need to do reverse image searching.

```
- Note: You shouldn’t search manually for all Hilton hotels, because there are too many Hilton hotels around the world! And that’s why I’ve chosen a Hilton hotel (because I don’t want you to guess anything).
```
<br/><br/>

One of the best sites to do reverse image searching is **Yandex** (https://yandex.com/images/)
<br/><br/>
![-023](https://user-images.githubusercontent.com/70543460/92233627-4a3b9280-eeb9-11ea-9637-969cedad885d.png)

<br/><br/>

You’ll find that the hotel is in Montenegro.
<br/><br/>
![-024](https://user-images.githubusercontent.com/70543460/92233652-56bfeb00-eeb9-11ea-98f2-7d17b5f34909.png)

<br/><br/>
...
<br/><br/>

Go to TripAdvisor and search for that hotel:
<br/><br/>
![-025](https://user-images.githubusercontent.com/70543460/92233809-a0103a80-eeb9-11ea-9d76-a9b026563ab4.png)
<br/><br/>

https://www.tripadvisor.com/Hotel_Review-g304088-d600703-Reviews-Hilton_Podgorica_Crna_Gora-Podgorica_Podgorica_Municipality.html

Go to the reviews and you will find this one:

![-026](https://user-images.githubusercontent.com/70543460/92233857-b74f2800-eeb9-11ea-86ce-c84fd2344a59.png)
<br/><br/>

As you see, Eword is mentioned in the review, so this is the person who are you looking for!

-----

Now you need to find a flag in one of his social media accounts
**(That was mentioned in the Pastebin link that you found before)**
<br/><br/>
![-027](https://user-images.githubusercontent.com/70543460/92233908-ccc45200-eeb9-11ea-9665-fd2e7f13f896.png)
<br/><br/>
...
<br/><br/>
I don’t want you to guess anything. So, I changed the TripAdvisor username of Eword leader to: (check_my_instagram)

![-028](https://user-images.githubusercontent.com/70543460/92233962-e1084f00-eeb9-11ea-9fb2-c9681b993789.png)
<br/><br/>

So, you need to find his Instagram account, and you can do that in 2 ways:

1. Search for his name in Instagram.

**or**

2. You’ll find his username in his TripAdvisor bio too:
<br/><br/>
![-029](https://user-images.githubusercontent.com/70543460/92234043-0301d180-eeba-11ea-84e5-d0e78fec0dd7.png)
<br/><br/>

https://www.instagram.com/wokaihwokomaskustermann/

<br/><br/>

-----

Check the story highlights in his Instagram account, you will find 2 stories:
<br/><br/>
![-030](https://user-images.githubusercontent.com/70543460/92234094-1ca31900-eeba-11ea-808d-acfde673d769.png)
<br/><br/>
![-031](https://user-images.githubusercontent.com/70543460/92234106-23319080-eeba-11ea-8f4e-586e8003d086.png)
<br/><br/>
<br/><br/>

The second highlighted story is a hint about the flag location.

**So, check his Instagram full sized profile picture and you will get the flag.**

<br/><br/>

```
There are a lot of sites/ methods to do that,
Example:
https://www.instadp.com/
```

![-032](https://user-images.githubusercontent.com/70543460/92234334-83c0cd80-eeba-11ea-8762-25b629fc5f56.png)

-----

# Fun facts:

- The pictures of Fred and Wokaihwokomas are for people who don't exist!
```
For more details, read more about (thispersondoesnotexist.com)
```
<br/><br/>
![Fred Bloggs](https://user-images.githubusercontent.com/70543460/92234765-49a3fb80-eebb-11ea-8d18-3e1fe0ff2472.png)
<br/><br/>
![Wokaihwokomas Kustermann](https://user-images.githubusercontent.com/70543460/92234787-5294cd00-eebb-11ea-9a28-b18d26fe3d52.png)
<br/><br/>

<br/><br/>

- **"Fred Bloggs"** is a placeholder name!
```
Placeholder names are words that can refer to objects or people whose names do not exist, are temporarily forgotten, irrelevant, or unknown in the context in which they are being discussed.
```
<br/><br/>
![image](https://user-images.githubusercontent.com/70543460/92235003-a7384800-eebb-11ea-946b-cfb8317c8fb5.png)
<br/><br/>

<br/><br/>

- **"Wokaihwokomas Kustermann"** is generated using a fake name generator!
