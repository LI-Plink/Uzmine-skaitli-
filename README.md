import random
import time

def sveiciens():
    vards = input("Ievadi savu vārdu: ")
    print(f"Sveiks, {vards}!")
    return vards
3
def uzmini_skaitli():
    pareizais = random.randint(1, 10)
    minejums = int(input("Uzmini skaitli no 1 līdz 10: "))
    if minejums == pareizais:
       print("Apsveicu! Tu uzminēji!")
    else:
       print(f"Tu neuzminēji. Pareizais skaitlis bija {pareizais}.")

def vai_turpinat():
    atbilde = input("Vai vēlies mēģināt vēlreiz? (j/n): ").lower()
    return atbilde == 'j'

def galvena_funkcija():
    saksanas_laiks = time.time()
    sveiciens()
    while True:
        uzmini_skaitli()
        if not vai_turpinat():
            break

    beigsanas_laiks = time.time()
    ilgums = round(beigsanas_laiks - saksanas_laiks, 2)
    print(f"Paldies par spēli! Programma darbojās {ilgums} sekundes.")

if __name__ == "__main__":
    galvena_funkcija()
