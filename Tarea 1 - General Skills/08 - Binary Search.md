## Descripción
Want to play a game? As you use more of the shell, you might be interested in how they work! Binary search is a classic algorithm used to quickly find an item in a sorted list. Can you find the flag? You'll have 1000 possibilities and only 10 guesses.Cyber security often has a huge amount of data to look through - from logs, vulnerability reports, and forensics. Practicing the fundamentals manually might help you in the future when you have to write your own tools!You can download the challenge files here:

- [challenge.zip](https://artifacts.picoctf.net/c_atlas/5/challenge.zip)

Additional details will be available after launching your challenge instance.

`ssh -p 50399 ctf-player@atlas.picoctf.net`Using the password `1ad5be0d`. Accept the fingerprint with `yes`, and `ls` once connected to begin. Remember, in a shell, passwords are hidden!
## Pistas
Have you ever played hot or cold? Binary search is a bit like that.

You have a very limited number of guesses. Try larger jumps between numbers!

The program will randomly choose a new number each time you connect. You can always try again, but you should start your binary search over from the beginning - try around 500. Can you think of why?

## Solución 1
Reduciendo los saltos entre numeros...
```shell
Welcome to the Binary Search Game!

I'm thinking of a number between 1 and 1000.

Enter your guess: 500

Higher! Try again.

Enter your guess: 800

Lower! Try again.

Enter your guess: 700

Higher! Try again.

Enter your guess: 750

Higher! Try again.

Enter your guess: 775

Higher! Try again.

Enter your guess: 783

Higher! Try again.

Enter your guess: 790

Congratulations! You guessed the correct number: 790

Here's your flag: picoCTF{g00d_gu355_3af33d18}

Connection to atlas.picoctf.net closed.
    ```

## Notas adicionales

## Referencias
