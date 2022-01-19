# Python_Image-Steganography
<div align="center"><img src="https://www.google.com/url?sa=i&url=https%3A%2F%2Ftowardsdatascience.com%2Fsteganography-hiding-an-image-inside-another-77ca66b2acb1&psig=AOvVaw2ldv6IHeZ4bkme58ZPIAuA&ust=1642655503494000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCNjK0OGGvfUCFQAAAAAdAAAAABAD"/></div>   
		
</div>

# Image Steganography
Steganography is the process of hiding a secret message within a larger one in such a way that someone  cannot know the presence or contents of the hidden message. Although related, Steganography is not to be confused with Encryption, which is the process of making a message unintelligible—Steganography attempts to hide the existence of communication.
The main advantage of steganography algorithm is because of its simple security mechanism. Because the steganographic message is integrated invisibly and covered inside other harmless sources, it is very difficult to detect the message without knowing
the existence and the appropriate encoding scheme .

## Encoding Algorithm
- Firstly, the secret message that is extracted is `compressed` as the contents in the compressed string will significantly hard to detect and read, furthermore it reduces the size of string.
- Secondly, the compressed string is `encrypted` with the secret key.
- Finally, `encoding` the encrypted message in the image. It uses `LSB steganographic embedding` to encode data into an image. Once the message is encoded the process stops.
### LSB(Least Significant Bit) Embedding
The LSB is the lowest significant bit in the byte value of the image pixel.
The  LSB  based  image  steganography  embeds  the  secret  in the  least  significant  bits  of  pixel  values  of  the  cover  image (CVR).
The concept of LSB Embedding is simple. It exploits the fact that the level of precision in many image formats is far greater than that perceivable by average human vision. Therefore, an altered image with slight variations in its colors will be indistinguishable from the original by a human being, just by looking at it. In conventional LSB technique, which requires eight bytes of pixels to store 1byte of secret data but in proposed LSB technique, just four bytes of pixels are sufficient to hold one message byte. Rest of the bits in the pixels remains the same.


## Decoding Algorithm
- Firstly, `decode` the message from the encrypted image using LSB decoding.

- Secondly, `decrypt` the compressed message from the decoded message using the secret key.

- Finally, `decompress` the message to get the original compressed message.   


# The Flow of the Application is as follows:
<img width="370" alt="1" src="https://user-images.githubusercontent.com/61881158/150067205-a31a84e1-1104-4362-9ddb-e450994e6c53.png">
<img width="370" alt="2" src="https://user-images.githubusercontent.com/61881158/150067207-0540b9e2-f65b-4fb2-bfb9-d219a691f84f.png">
<img width="370" alt="3" src="https://user-images.githubusercontent.com/61881158/150067209-1e4d8d97-df1d-421f-8de1-da3334b51ccb.png">
<img width="370" alt="4" src="https://user-images.githubusercontent.com/61881158/150067211-01e60e79-d1c1-4bc0-bad5-4728b7ee0bd0.png">
<img width="370" alt="5" src="https://user-images.githubusercontent.com/61881158/150067216-ae68c3bf-5a6b-45af-b4ce-f5b6b081a257.png">
<img width="370" alt="6" src="https://user-images.githubusercontent.com/61881158/150067218-1a098c42-ccdc-417b-b206-f624cc5e093d.png">
