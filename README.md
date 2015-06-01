import sys
codeseen = True
key = True


def loss():
    print "YOUR DEAD LMAO!!!"
    FirstRoom()

def LATA():
    print "You OUTIE! LATAAAAAAAAAAAAAAAAAAAAAA"
    sys.exit()




    
    
def Start():
    print "You are alone in a spooky dungeon, atleast thats what you think."
    print "You know you have to get out of here before you get too spooked and die"
    print "There are four doors in each of the four directions, North, South, East, West."
    print "Which way do you wish to go?"
    FirstRoom()

def zombie():

    
    choice = raw_input()
    if choice == "1337":
        print "the Door opens to reaveal Zombie looking monster things in test tubes,"
        print " you have the option to release them, should you Y/N "

        choice2 = raw_input()
        print choice2
        if choice2 == "y":
            print "The Zombies Are Realeased"
            print "They Begin Chanting And Surround You"
            print "would you like to run now? Y/N"
            choice3 = raw_input()
            if choice3 == "y":
                print "The Zombies Find Your Lack Of Trust Disturbing And Kill You."
                loss()
            if choice3 == "n":
                print "The Zombie Leader Aproaches..."
                print "\"Hello, My Name Is Bjergsen, Thank You For Releasing Me And My Legion, We Will Now Escort You Out Of Here.\""
                LATA()
            else:
                print "invalid command Try agin"
                zombie()
                
            

        elif choice2 == "n":
            print "You Run Away"
            Start()
            
        else:
            print "invalid command Try agin"
            zombie()

    else:
        print "You Typed The Wrong Code"
        print "        Try again       "
        zombie()
    

def FirstRoom():
    print "You are at the start of the dungeon, Go north, south, east, west."
    choice = raw_input()

    if choice == "west":
        WestStart()
    elif choice == "north":
        print "Die"
    elif choice == "east":
        print "Die"
    elif choice == "south":
        print "Die"
    else:
        print "sorry that is not a valid option, please try again"
        FirstRoom()




def WestStart():
    global codeseen

    print "You aproach the door to a more high tech looking"
    print "area of the dungeon, the door requires a code."
    if codeseen == False:
        print "you should probably find a code first, you have to go back."
        FirstRoom()    
    if codeseen == True:
        print "Type the code?"
        zombie()
                
        
Start()

