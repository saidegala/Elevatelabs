# 🔐 Password Complexity & Security Evaluation

This project explores how password complexity impacts security. We generate multiple passwords of varying strength, test them using password strength checkers, and summarize best practices and risks related to weak password usage.

---

## ✅ 1. Create Multiple Passwords with Varying Complexity

We created the following example passwords with differences in length, character sets, and patterns:

| Password            | Characteristics                          |
|---------------------|-------------------------------------------|
| `password123`       | Lowercase + digits                        |
| `Pass1234`          | Mixed case + digits                       |
| `P@ssw0rd!`         | Mixed case + digits + symbol              |
| `xYz#91@Lm*Qz`      | High complexity, 12 characters            |
| `CorrectHorseBatteryStaple` | Long passphrase, easy to remember  |

---

## 🧪 2. Password Strength Testing

We tested each password using popular password strength checkers like:

- [Kaspersky Password Checker](https://password.kaspersky.com)
- [NordPass Strength Test](https://nordpass.com/password-strength-checker/)
- [How Secure Is My Password?](https://howsecureismypassword.net/)

---

## 📊 3. Strength Scores & Feedback

| Password                  | Estimated Crack Time    | Feedback Summary                           |
|---------------------------|-------------------------|---------------------------------------------|
| `password123`             | <1 second               | Very weak, common, easy to guess            |
| `Pass1234`                | Few seconds             | Still weak, uses common words + patterns    |
| `P@ssw0rd!`               | Several hours           | Better, includes symbols, still predictable |
| `xYz#91@Lm*Qz`            | Many years              | Strong, random, good complexity             |
| `CorrectHorseBatteryStaple` | Centuries              | Very strong due to length, easy to remember |

---

## 💡 4. Password Best Practices (Learned Tips)

- Use at least **12 characters**.
- Combine **uppercase, lowercase, numbers, and symbols**.
- Avoid **common words**, dictionary patterns, and substitutions (`P@ssw0rd` is still predictable).
- Consider using a **passphrase** (e.g., `BlueDragonSky!47`).
- Don’t reuse passwords across multiple sites.
- Use a **password manager** to store and generate strong, unique passwords.

---

## 🛡️ 5. Common Password Attacks

| Attack Type     | Description                                                                 |
|------------------|-----------------------------------------------------------------------------|
| **Brute Force**  | Tries all possible combinations. Longer, complex passwords help mitigate.  |
| **Dictionary**   | Uses precompiled lists of common passwords/phrases. Avoid using real words.|
| **Credential Stuffing** | Uses known breaches to try logins on other services. Avoid reuse.   |

---

## 🔐 6. Why Password Complexity Matters

Password complexity directly affects how resistant your password is to being guessed or cracked. Complex passwords increase the number of possible combinations, making **brute force attacks slower** and **dictionary attacks ineffective**. While simple passwords are easier to remember, they offer very poor protection in the modern threat landscape. A strong, complex password is essential for securing personal and sensitive information.

---

## 📁 Repository Structure

