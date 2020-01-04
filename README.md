# spotify-observer
Spotify Observer App

## Setup

### Generate JWT private & public keys

- Generate a RSA private key:  
  `openssl genrsa -out private.pem 2048`
- Export the public key:  
  `openssl rsa -in private.pem -outform PEM -pubout -out public.pem`

Open `private.pem` and `public.pem` in a text editor and replace all newlines with the text `\n` so each file becomes
one continuous string.
Copy the string from `private.pem` into `.env` with key `JWT_PRIVATE_KEY_PEM`.
Copy the string from `public.pem` into `.env` with key `JWT_PUBLIC_KEY_PEM`.

## Useful reading

- https://gist.github.com/gitaarik/8735255