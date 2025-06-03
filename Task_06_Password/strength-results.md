# 🔐 Password Strength Results

Passwords were tested using:
- https://password.kaspersky.com
- https://nordpass.com/password-strength-checker/
- https://howsecureismypassword.net

| Password                  | Estimated Crack Time    | Feedback                                     |
|---------------------------|-------------------------|----------------------------------------------|
| `password123`             | Less than 1 second      | Very weak. Common and predictable.           |
| `Pass1234`                | A few seconds           | Weak. Still uses common patterns.            |
| `P@ssw0rd!`               | Several hours           | Moderate. Improved complexity, still guessable. |
| `xYz#91@Lm*Qz`            | Hundreds of years       | Strong. Randomized and complex.              |
| `CorrectHorseBatteryStaple` | Centuries             | Very strong. High entropy due to length.     |

> ⚠️ Note: "P@ssw0rd" types are often found in leaked password lists, despite added symbols.
