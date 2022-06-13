# rock-paper-scissors
Python code for rock paper scissors
import random
#rock paper scissor game
print('welcome to the Rock, Paper, Scissors Game')
running = True
while running:
    possible_response = ['R','P','S']
    computer_response=(random.choice(possible_response))
    user_response=input('enter your choice for R,P,S: ')
    
    if user_response not in possible_response:
          print('Error')
    else:
          print(user_response)
    
    
    if user_response==computer_response:
        print(f'\n Player ({user_response}) : CPU ({computer_response})')
        print('There is a tie \n Nobody wins')  
    elif  user_response == 'P' and computer_response == 'S':
          print(f'\n Player ({user_response}) : CPU ({computer_response})')
          print('You have been cut in pieces...you failed \n The computer wins')
    elif user_response == 'S' and computer_response == 'P':
          print(f'\n Player ({user_response}) : CPU ({computer_response})')
          print('Sliced ..nice cut,way to go! \n You win')
    elif user_response == 'S' and computer_response == 'R':
          print(f'\n Player ({user_response}) : CPU ({computer_response})')
          print('You have been smashed \n The computer wins')
    elif user_response == 'R' and computer_response == 'S':
          print(f'\n Player ({user_response}) : CPU ({computer_response})')
          print('You smashed..yayy! \n You win')
          
    elif user_response == 'R' and computer_response == 'P':
          print(f'\n Player ({user_response}) : CPU ({computer_response})')
          print('You got covered by paper \n The computer wins')
    elif user_response == 'P' and computer_response == 'R':
          print(f'\n Player ({user_response}) : CPU ({computer_response})')
          print('You covered the rock \n You win')    
    
    play_again = input("Play again? (y/n): ")
    if play_again.lower() != "y":
          break
