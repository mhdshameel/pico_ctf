Dolls

given an image file : ![dolls](https://github.com/mhdshameel/pico_ctf/assets/16662695/d1d36890-5518-4d47-be3c-7d844237d1cc)

And the clue as:
Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one?

The clue clearly indicates that the file could contain other files:
Immediately openend the image with 7zip file manager and we can see there is a nested folder 'base_images'.
From that came 2_c.jpg.
And again that file contained 3_c.jpg

And nested contains a text file flag.txt
