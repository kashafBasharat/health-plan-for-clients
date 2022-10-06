# health-plan-for-clients


def gettime():
    import datetime
    return datetime.datetime.now()


def log():
    print("Choose your client")
    client = int(input("1. Amna \n2. Ammaila \n3. Kashaf"))
    con = 1
    if client == 1:
        while con == 1:
            print("What do you want to log for Amna?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("amna diet.txt", "a")
                data = input("Enter what has Amna Eaten?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()

            else:
                f = open("amna exercise.txt", "a")
                data = input("How much time has Amna worked out?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()
            con = int(input("Do you want to log more for Amna? \n1. Yes \n2. No"))

    elif client == 2:
        while con == 1:
            print("What do you want to log for Ammaila?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("ammaila diet.txt", "a")
                data = input("Enter what has Ammaila Eaten?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()

            else:
                f = open("ammaila exercise.txt", "a")
                data = input("How much time has Ammaila worked out?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()
            con = int(input("Do you want to log more for Ammaila? \n1. Yes \n2. No"))

    elif client == 3:
        while con == 1:
            print("What do you want to log for Hammad?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("hammad diet.txt", "a")
                data = input("Enter what has Hammad Eaten?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()

            else:
                f = open("kashaf exercise.txt", "a")
                data = input("How much time has Kashaf worked out?")
                f.write(str([str(gettime())]) + "  " + data + "\n")
                f.close()
            con = int(input("Do you want to log more for Kashaf? \n1. Yes \n2. No"))


def retrieve():
    con = 1
    while con == 1:
        print("Choose your client")
        client = int(input("1. Amna \n2. Ammaila \n3. Kashaf"))
        if client == 1:
            print("What do you want to retrieve for Amna?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("amna diet.txt", "r")
                print(f.readlines())
                f.close()

            else:
                f = open("amna exercise.txt", "r")
                print(f.readlines())
                f.close()

        elif client == 2:
            print("What do you want to retrieve for Ammaila?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("ammaila diet.txt", "r")
                print(f.readlines())
                f.close()

            else:
                f = open("ammaila exercise.txt", "r")
                print(f.readlines())
                f.close()

        elif client == 3:
            print("What do you want to retrieve for Kashaf?")
            choice = int(input("1. Diet \n2. Activity"))
            if choice == 1:
                f = open("Kashaf diet.txt", "r")
                print(f.readlines())
                f.close()

            else:
                f = open("kashaf exercise.txt", "r")
                print(f.readlines())
                f.close()
    con = int(input("Do you want to retrieve any more details? \n1. Yes \n2. No"))


print("Welcome to Health care Management System")
ch = int(input("What do you want to do? \n1. Log \n2. Retrieve"))
if ch == 1:
    log()
elif ch == 2:
    retrieve()
else:
    print("Wrong Input. Please try again.")
