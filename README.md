# Ljupcho Toshev 203128
# Control Flow Graph
![cfg](https://github.com/ljupchotoshev/SI_2023_lab2_203128/assets/98028371/534da630-15a0-4d25-84f6-3445f3b47f65)

[код](https://i.imgur.com/COPeolp.png)
# Цикломатска комплексност
Цикломатската комплексност на овој код е 11, ја добив со формулата Р+1, каде што P е бројот на предикатни јазли. 
# Тест случаи според критериумот Every Branch
Тест случај за недостасување на задолжителни информации:

User објект: null -
Треба да се фрли RuntimeException со пораката "Mandatory information missing!"

Тест случај кога user.getUsername() е null:

User објект: new User("email@email.com", "password123", null) -
Корисничкото име на User објектот треба да биде поставено на е-поштата ("email@email.com").

Тест случај кога user.getEmail().contains("@") и user.getEmail().contains(".") враќаат false:

User објект: new User("email@email.com", "password123", "username") -
Променливата same треба да остане 1.

Тест случај за user.getEmail().contains("@") и user.getEmail().contains(".") кои враќаат true, и ниту еден корисник во листата нема иста е-пошта или корисничко име:

User објект: new User("email@email.com", "password123", "username") -
Променливата same треба да биде 0.

Тест случај за user.getEmail().contains("@") и user.getEmail().contains(".") кои враќаат true, и постои корисник во листата со иста е-пошта или корисничко име:

User објект: new User("email@email.com", "password123", "username") -
Променливата same треба да биде зголемена за 1.

Тест случај за passwordLower.contains(user.getUsername().toLowerCase()) кој враќа true:

User објект: new User("email@email.com", "username123", "username") -
Функцијата треба да врати false, бидејќи лозинката го содржи корисничкото име.

Тест случај за password.length()<8 кој враќа true:

User објект: new User("email@email.com", "pswd!", "username") -
Функцијата треба да врати false, бидејќи лозинката е помала од 8 карактери.

Тест случај кога !passwordLower.contains(" ") враќа false:

User објект: new User("email@email.com", "password 123!", "username") -
Функцијата треба да врати false, бидејќи лозинката содржи празно место.

Тест случај за валидна лозинка без посебни знаци:

User објект: new User("email@email.com", "password123", "username") -
Функцијата треба да врати false, бидејќи same не е 0.

Тест случај за валидна лозинка со посебни знаци:

User објект: new User("email@email.com", "password123!", "username") -
Функцијата треба да врати true, бидејќи same е 0 и лозинката содржи посебен знак.
# Тест случаи според критериумот Multiple Conditions

