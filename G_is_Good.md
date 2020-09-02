# G is Good (OSINT - 500 points)

![-000](https://user-images.githubusercontent.com/70543460/91977493-6dd0d280-ed2b-11ea-927c-18b0225fa82e.png)

<br/><br/>

# Solution:

According to the description, R****** and his friend **only use Google products**. Also, we have an email address in the description.

-----

```diff
- Note: You won’t get anything if you send anything to the email address.
```

-----

The idea of the first step is getting the Google ID of that email address.

```diff
- Note: I know that not everyone knows this, but simple googling will give you the answer.
```

![-001](https://user-images.githubusercontent.com/70543460/91978595-0e73c200-ed2d-11ea-9097-65871e84eef5.png)

-----

The easiest way to get the Google ID of that email address is by using Google Contacts (https://contacts.google.com/)

1. Create a new contact with that email address.
2. Press (F12) to open the inspect element window.
3. Go to the Network tab and clear everything there.
<br/><br/>
![-002](https://user-images.githubusercontent.com/70543460/91978800-6d393b80-ed2d-11ea-9aba-e6186fc329cb.png)
<br/><br/>
4. When you have a blank network activities screen, go back to the Google Contacts page, and click on the contact.
5. In the network window, we need the packet that begins with batchexecute, so click on it to get its contents.
6. Scroll to the bottom of the Headers tab, you will find the field Form Data, then you will find the 21-digit Google ID.
<br/><br/>
![-004](https://user-images.githubusercontent.com/70543460/91978854-804c0b80-ed2d-11ea-8843-feb256e0ed5b.png)
<br/><br/>

So, the Google ID of i.am.not.richard.roe@gmail.com is:
**111847369296165457396**

-----

Using the Google ID, we can find the **Google Maps Contributions** of that email address.

```diff
https://www.google.com/maps/contrib/(Google ID)
```

So, when you open
https://www.google.com/maps/contrib/111847369296165457396
You will get:

- The name of the owner of that email address. (Richard Roe)
(You will need it in the next step)
- The picture of the owner of that email address.
(You will need it in the next step)
<br/><br/>
![-005](https://user-images.githubusercontent.com/70543460/91979206-1718c800-ed2e-11ea-953b-2aef9901cfd6.png)
<br/><br/>
- The places reviews that the owner of that email address has written.
(You will need in the last step)
<br/><br/>
![-006](https://user-images.githubusercontent.com/70543460/91979277-33b50000-ed2e-11ea-9856-1e853aa9bd4c.png)
<br/><br/>

You will see that Richard has 1 contribution. He has rated a **language school** in **Bosnia and Herzegovina**.
<br/><br/>
![-007](https://user-images.githubusercontent.com/70543460/91979452-77a80500-ed2e-11ea-92bc-6219880bbd63.png)
<br/><br/>
![-008](https://user-images.githubusercontent.com/70543460/91979471-85f62100-ed2e-11ea-97cd-04b843d980c8.png)
<br/><br/>

```diff
- Remember: In OSINT, locations are important.
```

-----

Now, you need to find Richard Roe in another site…
You might think that this step is guessy, **but it’s not**, because I have already given you a sentence (in the description) that will reduce your searching scope:

```
BTW, we only use Google products and we don’t use any site that doesn’t belong to Google... LITERALLY!
```

The right place to continue solving this challenge is Youtube.

```diff
- Note: YouTube belongs to Google.
```

I know that you don’t know the name of his channel in Youtube, but if you search for his name in Youtube, you will find it.
(Don’t forget to use search filters)
<br/><br/>
![-010](https://user-images.githubusercontent.com/70543460/91979963-395f1580-ed2f-11ea-8a9c-78f32c84c3c8.png)
<br/><br/>
So, search for his name and scroll down until you find a channel with his picture that you have already seen in Google Maps.
<br/><br/>
![-011](https://user-images.githubusercontent.com/70543460/91980011-4b40b880-ed2f-11ea-8dd0-1ba054b84655.png)
<br/><br/>

Open his channel and you will see one uploaded video and one featured channel:
<br/><br/>
![-012](https://user-images.githubusercontent.com/70543460/91980073-61e70f80-ed2f-11ea-82ed-a2a964721ce8.png)
<br/><br/>

Focus on the featured channel name **(John Doe)**… It is clear that John is his best friend who is mentioned in the challenge description.

```
My best friend enjoys hiding secret messages in the internet!
```

So, you won’t find anything in Richard channel... You will only need it to find his best friend channel.
<br/><br/>
Open John’s channel, you will find one uploaded video
<br/><br/>
![-013](https://user-images.githubusercontent.com/70543460/91980249-9d81d980-ed2f-11ea-9203-4f5b4169c618.png)
<br/><br/>

This video contains a Morse Code that won’t give you the flag when you decode it (It’s a rabbit hole).
So, I added this clarification in the video description:
<br/><br/>
![-014](https://user-images.githubusercontent.com/70543460/91980362-d0c46880-ed2f-11ea-92a6-26907d7f2719.png)
<br/><br/>

-----

According to the description, John always travels with Richard.

```
And my best friend always travels with me.
```

And you already have a location… (remember the Google Maps review).

And that place was a language school in Bosnia and Herzegovina.

So, they might have been learning a foreign language, and that language may be Bosanski because they were in Bosnia and Herzegovina.

-----

<br/><br/>
**You are now in the last step of this challenge: Getting the Flag.**
<br/><br/>

To get the flag you need to find a relationship between everything you have got!
(Youtube + Bosnia and Herzegovina + Languages + Hiding messages)
<br/><br/>

One of the best things in youtube is that you can translate your videos titles and descriptions.
<br/><br/>
![-015](https://user-images.githubusercontent.com/70543460/91980635-3f092b00-ed30-11ea-8e09-358d2d65fa38.png)
<br/><br/>

1. Go to the video in John’s channel (because he hides the messages)
2. Change the Youtube language to Bosanski (because they have gone to language school in Bosnia and Herzegovina)
3. You will find the flag in the description of that video.
<br/><br/>
![-016](https://user-images.githubusercontent.com/70543460/91980688-53e5be80-ed30-11ea-82de-71990d5fde17.png)
<br/><br/>

-----

# Important notes:

- The main idea of this challenge is linking everything you get together.

- To those who say that the idea of the first step of this challenge was in a challenge in another platform/CTF: An idea of a step may be in other platforms and there is no problem in mixing ideas, because this is a CTF, so the main goal is to learn new ideas **(even if they are mixed with other ideas).** So, please compare all the steps and the whole scenario and the contents of the challenge, and don't compare only one step!!!

-----

# Fun facts:

- The pictures of Richard and John are for people who don't exist!
```
For more details, read more about (thispersondoesnotexist.com)
```
<br/><br/>
![thispersondoesnotexist](https://user-images.githubusercontent.com/70543460/92025580-6f6cbb80-ed68-11ea-8a98-3cf9be333d09.png)
<br/><br/>
![thispersondoesnotexist2](https://user-images.githubusercontent.com/70543460/92025602-7a275080-ed68-11ea-87f8-a7056f20007e.png)
<br/><br/>

<br/><br/>

- **"Richard Roe"** and **"John Doe"** are placeholder names!
```
Placeholder names are words that can refer to objects or people whose names do not exist, are temporarily forgotten, irrelevant, or unknown in the context in which they are being discussed.
```
<br/><br/>
![image](https://user-images.githubusercontent.com/70543460/92026250-692b0f00-ed69-11ea-8c81-4ff8e4edd885.png)
<br/><br/>
