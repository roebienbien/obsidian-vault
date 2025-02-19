2024-09-25 10:06

Status: #idea

Tags: [[programming]]

# jwt

**JSON Web Token (JWT)** is a widely used open standard (RFC 7519) for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

## JWT Structure

A JWT typically consists of three parts separated by dots (`.`):

1. **Header**:
   - Specifies the type of the token (JWT) and the signing algorithm being used (e.g., HMAC, RSA, ECDSA).
   - Example: 
     ```json
     {
       "alg": "HS256",
       "typ": "JWT"
     }
     ```

2. **Payload**:
   - Contains the claims, which are statements about an entity (typically the user) and additional data. Claims are either registered, public, or private claims.
   - Example:
     ```json
     {
       "sub": "1234567890",
       "name": "John Doe",
       "admin": true
     }
     ```

3. **Signature**:
   - This is the result of signing the encoded header and payload with the secret or private key using the specified algorithm. The signature allows the receiver to verify the integrity of the token and ensure it hasn't been tampered with.

## Signing Algorithms

- **[[HMAC]] (HS256, HS512)**: Uses a shared secret between the two parties to sign and verify the JWT.
- **[[RSA]] (RS256, RS512)**: Uses a public/private key pair. The sender signs the JWT with their private key, and the recipient verifies it using the sender’s public key.
- **[[ECDSA]] (ES256, ES512)**: Similar to RSA but uses elliptic curve cryptography for signing.

## Common Use Cases

- **Authentication**: Once a user is authenticated, a JWT can be issued and used to verify the user’s identity on subsequent requests.
- **Authorization**: JWTs can carry roles or permissions information, which can be used to grant access to resources.
- **Data Exchange**: Since JWTs can be signed and optionally encrypted, they are a secure way to exchange information between parties.

## Key Advantages

- **Compact**: JWTs are small in size and can easily be transmitted via URL, POST parameters, or inside HTTP headers.
- **Self-contained**: All the information needed for authentication or authorization is embedded within the token itself, reducing the need to make repeated database queries.

## Security Considerations

- JWTs are not encrypted by default, which means sensitive information should not be stored in the payload unless the token is encrypted (JWE - JSON Web Encryption).
- Properly managing the secret keys or public/private keys is essential to maintain the security of the JWT system.



