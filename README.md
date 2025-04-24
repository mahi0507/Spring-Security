🔐 JWT Auth Flow – Brief Summary
1. Login API (/login)
Tu username/password bhejta hai.

Agar valid hai → JWT token generate hota hai.

Response me token milta hai.

2. JWT Token
JwtUtil class token banata hai.

Token ke andar username + expiry hota hai.

3. JWT Filter (JwtRequestFilter)
Har request ke saath token check karta hai.

Agar token valid hai → user ko authenticate karta hai.

4. Security Config
/login public hai.

Baaki endpoints protected hai → JWT token mandatory.

5. Protected Endpoint (/user/data)
Token valid hai toh hi access milega.

Nahi toh ❌ unauthorized.

6. Hardcoded User
Username: user1

Password: password

