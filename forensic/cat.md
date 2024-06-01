The file provided:
![cat](https://github.com/mhdshameel/pico_ctf/assets/16662695/ef438ba9-a663-4f91-b3a9-ca4247867cae)

Initial impression after seeig the file is that some file is embedded into the image. Opened it in text viewer and saw the initial few bytes.
![image](https://github.com/mhdshameel/pico_ctf/assets/16662695/fdcb8b5b-e5e4-4bb6-b971-c2ac067dc83c)

The magic byte seems to be different but we can still see the JFIF.
Used the `file` tool to check the actual file type of this file:
![image](https://github.com/mhdshameel/pico_ctf/assets/16662695/ba8a663d-98f5-49cc-9d8d-a1d1291dced3)
And can see that the file is a genuine jpeg file.

But in the text viewer output of the file we can note that there is mention of a "ExifTool 10.80". A basic search reveals that this tool is used to edit the metadata of any file.
The tool can be used to read/write the metadata.
Downloaded it and used it to read the metadata of this file and we can see the following output

![image](https://github.com/mhdshameel/pico_ctf/assets/16662695/148b0868-686f-4267-93c0-d1f4094de088)

And the license section contains some peculiar string. Could it be the base64 encoded flag and.. yes it is.

```cGljb0NURnt0aGVfbTN0YWRhdGFfMXNfbW9kaWZpZWR9```
decodes to : `picoCTF{the_m3tadata_1s_modified}`
