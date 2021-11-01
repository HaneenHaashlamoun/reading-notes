# Cryptography

![cryp](https://cdn-images-1.medium.com/max/1024/1*GeKaK4YBRRrw4EV-_1bXzw.png)

One of the earliest encryption techniques is the Caesar Cipher, invented by Julius Caesar more than two thousand years ago to communicate messages to his allies.
The Caesar Cipher is a great introduction to encryption, decryption, and code cracking, thanks to its simplicity.

## Encrypting a message

Imagine Caesar wants to send this message:

> SECRET MEETING AT THE PALACE

Here's what that might look like encrypted:

> YKIXKZ SKKZOTM GZ ZNK VGRGIK

### Caesar Cipher

![](https://unravellingsoftwaredevelopment.files.wordpress.com/2018/12/caesar_ciphercipher-e1546115341980.jpg?w=700)

## Decrypting a message

According to historical records, Caesar always used a shift of 3. As long as his message recipient knew the shift amount, it was trivial for them to decode the message.
Imagine Caesar sends this message to a comrade:

> EHZDUH EUXWXV

A	B	C	D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z

D	E	F	G	H	I	J	K	L	M	N	O	P	Q	R	S	T	U	V	W	X	Y	Z	A	B	C

They can then decode the message with certainty. The first letter "E" was shifted by 3 from "B", the second letter "H" was shifted by 3 from "E", etc. The result is this ominous message:

> BEWARE BRUTUS


![crypt](https://cdn.shortpixel.ai/spai/w_690+q_lossy+ret_img+to_webp/https://thebestvpn.com/wp-content/uploads/2017/06/lead_960.jpg)

## Cracking the cipher

### Frequency analysis
There are three main techniques he could use: frequency analysis, known plaintext, and brute force.

Human languages tend to use some letters more than others. For example, "E" is the most popular letter in the English language. We can analyze the frequency of the characters in the message and identify the most likely "E" and narrow down the possible shift amounts based on that.

### Known plaintext

Another term for the original unencrypted message is plaintext. If the enemy already knew some part of the plaintext, it will be easier for them to crack the rest of the encrypted version.
For example, messages tend to start with similar beginnings. In WWII, encrypted German messages always started with a weather forecast, which ultimately made them easier for British mathematician Alan Turing to crack.

### Brute force

There are only 25 possible shifts (not 26 — why not?). The enemy could take some time to try out each of them and find one that yielded a sensible message. They wouldn't even need to try the shifts on the entire message, just the first word or two.

- Encryption: scrambling the data according to a secret key (in this case, the alphabet shift).
- Decryption: recovering the original data from scrambled data by using the secret key.
- Code cracking: uncovering the original data without knowing the secret, by using a variety of clever techniques.


## Types of Cryptography
![Types of Cryptography](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRQlbDnCVYeUOkUjMIX7pbQRX8-g6UlQuGUjg&usqp=CAU)

1. Hashing
2. Symmetric Cryptography
3. Asymmetric Cryptography
4. Key Exchange Algorithms

## The 4 Types of Cryptographic Functions

1. Authentication
2. Nonrepudiation
3. Confidentiality
4. Integrity


## Cryptography Isn’t Perfect

At this point, I hope that you have developed a concrete understanding of cryptography and its applications for everyday life.

But before I wrap up, I want to leave you with a word of warning.

While cryptography can certainly provide you with more security, it cannot provide you with total security.

With the plethora of attacks that have happened in recent years including the Tesco Bank, Department of Justice hack, and AdultFriendFinder attacks (just to name a few) it’s pretty clear that cryptography has its shortcomings.

And while the vast majority of you can sleep soundly knowing that large corporations are working their hardest to ensure the safe and secure transmission and storage of your data, it’s important to realize that you are not impervious to a similar attack.

This is not said to dissuade you from using the aforementioned methods of encryption, simply to inform you that even the best cryptographic algorithms were designed by imperfect teams of people and are subject to breach.

So as you go through your daily life, be mindful of this reality and realize that “More Secure” doesn’t mean “Totally secure”.

      
© Haneen Hashlamoun
