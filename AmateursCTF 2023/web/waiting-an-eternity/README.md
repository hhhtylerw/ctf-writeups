# waiting-an-eternity

## Prompt

My friend sent me this website and said that if I wait long enough, I could get and flag! Not that I need a flag or anything, but I've been waiting a couple days and it's still asking me to wait. I'm getting a little impatient, could you help me get the flag?

`waiting-an-eternity.amt.rs`

## Solution

The first page has a response header that contains information about the second page.

![1](image1.png)

The second page adds a cookie with a UNIX timestamp.

![2](image2.png)

Changing this value to `-inf` and refreshing gives the flag.

![3](image3.png)

## Flag

`amateursCTF{im_g0iNg_2_s13Ep_foR_a_looo0ooO0oOooooOng_t1M3}`
